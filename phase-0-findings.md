# Phase 0 — Findings

**Run:** August 2, 2026
**Status:** Complete. The blocker is solved; two caveats carried forward.

---

## 1. DCA district attribution — SOLVED

This was the blocker: CourtListener files all six District Courts of Appeal under a single court id, `fladistctapp`, and returns them all as "District Court of Appeal of Florida." Inter-district conflict is the engine of this doctrine, so nothing downstream works without district resolution.

### What was tested

| Method | Result |
|---|---|
| **(a) cluster → docket → `court` field** | **FAILED.** The docket record's `court_id` is also `fladistctapp`. `appeal_from` is null. No district anywhere on the docket. |
| **(b) docket-number regex** | **PARTIAL.** Works from roughly the early 2000s on (`3D08-2039`, `4D08-968`, `6D2023-2546`). Fails for the entire 1987–2000 era (`93-2778`, `94-04599`, `95-2012`) and for occasional modern records (`2023-0248`, `17-0174 & 17-0173 & 16-1692`). |
| **(c) opinion HTML header** | **WORKS** for the old corpus. |
| **(d) `download_url` hostname** | **WORKS** for the modern corpus. Discovered while closing the (b) gap. |

### Key discovery — `plain_text` is empty for old opinions

Pre-1996 Lawbox-sourced opinions return `plain_text: ""`. The text lives in `html_lawbox` and `html_with_citations` instead. Any text-based extraction that reads only `plain_text` silently returns nothing for the earliest and most important era.

Those fields carry a clean, centered district line:

```html
<center><p><b>District Court of Appeal of Florida, Fourth District.</b></p></center>
```

*(Verified on Mudano v. St. Paul Fire & Marine Ins. Co., 543 So. 2d 876 (Fla. 4th DCA 1989).)*

### Key discovery — `download_url` encodes the district

Modern opinions scraped from court sites carry a district-specific hostname:

```
https://2dca.flcourts.gov/pre_opinion_content_download/2438975
```

Verified on the one modern record that defeated docket parsing — *City of Sarasota v. Estate of Kaafi* (docket `2023-0248`). Hostname resolves to Second District; Sarasota County is in the Second District. Correct.

### Resolution — a four-signal cascade

Apply in order; stop at first hit.

| Signal | Source | Covers |
|---|---|---|
| **S1** | `download_url` hostname → `(\d)dca\.flcourts\.gov` | Modern scraped opinions |
| **S2** | `docketNumber` → `^(?:Nos?\.\s*)?(\d)D(\d{2}\|\d{4})-` | ~2000s → present |
| **S3** | `html_lawbox` / `html_with_citations` / `xml_harvard` → `District Court of Appeal of Florida,?\s+(First\|Second\|Third\|Fourth\|Fifth\|Sixth) District` | 1987 → ~2000 |
| **S4** | Judge panel → district lookup, or manual | Residual |

**Why this is robust:** the signals are independent, so wherever two are present they cross-validate. Build the cascade to record *which* signal fired for each case and log every disagreement — that gives a measurable confidence rate rather than an assumption.

### Note on S4

`panel_ids` and `panel_names` are mostly empty pre-1996, and the `judge` field is unreliable — *Palm Beach Polo Holdings* returns `"Ciklin, Had, Kaplan, Michael, Opportunity, Polen, Proceedings, Review"`, which is parser noise, not a panel. Treat S4 as manual review, not automation.

### A heuristic worth noting but NOT relying on

In the 1990s the Second District used five-digit zero-padded sequences (`94-04599`, `95-04027`, `94-02012`) while the Third and Fourth used four (`95-2012`, `95-1232`). Suggestive, not a rule. Use only to prioritize manual review, never as an attribution signal.

---

## 2. Corpus map — measured, not estimated

All figures are Florida state appellate opinions (`fla` + `fladistctapp`).

| Query | Count |
|---|---|
| `"768.79"` | **776** |
| `"1.442"` | **514** |
| `"768.79" OR "1.442"` | **901** |
| Florida **Supreme Court** only, union query | **85** |

### Distribution by era (`"768.79"`)

| Era | Count | Attribution tier |
|---|---|---|
| pre-1996 | 100 | S3 |
| 1996–2006 | 302 | S3 early, S2 late |
| 2006–2016 | 200 | S2 |
| 2016–2026 | 174 | S1 / S2 |

Buckets sum to exactly 776. Counts were independently validated by re-partitioning: 1996–2001 (161) + 2001–2006 (141) = 302, matching the combined bucket. **These are real counts, not pagination caps** — the round 100 and 200 figures were coincidence.

The Phase 1 estimate of 800–1,200 was accurate. **901 is the working universe.**

### The district-prefix transition is later than assumed

Sampling June 1996 – January 1997 returned *zero* district-prefixed docket numbers. The `ND{yy}-` format appears somewhere between 2000 and 2008 — not the mid-1990s. **Roughly 250–300 cases fall to S3**, not the ~100 originally assumed. S3 is therefore load-bearing, not a fallback, which is why the `plain_text`-is-empty discovery mattered.

---

## 3. Query set — locked

The terminology shift is confirmed and it is a real trap. Querying `"768.79" + "proposal for settlement"` returns 320 opinions with the earliest at **1997**. The statute dates to 1986. Adding `"offer of judgment"` recovers 65 pre-1996 cases reaching back to **1989** (*Mudano*).

**Retrieval procedure:** run `"768.79"` and `"1.442"` as independent sweeps, union them, then de-duplicate on `cluster_id`. Do not rely on phrase terms ("proposal for settlement," "offer of judgment," "demand for judgment") for *retrieval* — they belong in the coding layer as era markers, not the query layer.

---

## 4. Coding schema

| Field | Type | Notes |
|---|---|---|
| `cluster_id` | int | Primary key; de-dup on this |
| `opinion_id` | int | May differ from cluster_id |
| `case_name` | str | |
| `citation` | str | Preferred So.2d/So.3d cite |
| `date_filed` | date | |
| `court_level` | enum | `supreme` / `dca` |
| `district` | enum 1–6 | From the cascade |
| `district_signal` | enum | `S1`/`S2`/`S3`/`S4` — provenance |
| `district_confidence` | enum | `confirmed` (2+ signals agree) / `single` / `manual` |
| `panel` | str | |
| `issue_tags` | multi | The **ten** doctrinal arcs (listed in `CLAUDE.md`) — updated from six |
| `canon_invoked` | enum | `derogation` / `rule_1.010` / `both` / `neither` |
| `proposal_outcome` | enum | `upheld` / `invalidated` / `n-a` |
| `fee_disposition` | enum | `awarded` / `denied` / `remanded` |
| `conflict_certified` | bool | |
| `statute_version` | str | Which version of § 768.79 governed |
| `rule_version` | str | Which version of rule 1.442 governed |
| `subsequent_history` | str | Quashed / approved / receded from |
| `cite_count` | int | For tiering |

`statute_version` and `rule_version` are what make the two-track timeline work — they let you ask whether a case turned on text that no longer exists.

**Serialisation — CSV** (decision recorded August 4, 2026; the database is `case-database.csv`, not a spreadsheet binary):

- **UTF-8, RFC 4180**, header row, `\n` line endings. No BOM.
- `issue_tags` is the only multi-valued field. Encode as **semicolon-separated arc numbers**, ascending, no spaces — e.g. `1;3;4`. Semicolon rather than comma so the field never needs quoting for its own delimiter.
- Empty means *not applicable*; `unknown` means *not yet determined*. Keep those distinct — an empty `district` on a Supreme Court row is correct, whereas an undetermined DCA district is `unknown`.
- Dates ISO-8601 (`YYYY-MM-DD`). Booleans lowercase `true`/`false`.
- Case names contain commas and quotation marks constantly (*Willis Shaw Express, Inc. v. Hilyer Sod, Inc.*), so **quote every string field** rather than relying on a writer to decide. Escape embedded quotes by doubling.
- Diffs cleanly in Git, which a spreadsheet binary does not — that is the point of the format. Sort rows by `date_filed` so the diff stays legible.

### ✅ Built August 4, 2026 — `case-database.csv`, 87 rows × 24 columns

**Five columns were added to the schema above.** All five carry information the corpus already held and the original nineteen had nowhere to put:

| Added column | Why |
|---|---|
| `docket_number` | Six post-2020 opinions have **no reporter citation at all** (*CCM*, *Suarez Trucking*, *Trace Elements*, three rule opinions). Without this they are unidentifiable from the row |
| `vote` | The corpus's central structural finding is that the 4–3s cluster in one arc. Format follows `arc-matrix.md`: `4-3`, `7-0`, and `4-0+3` where justices concurred in result or wrote separately |
| `issue_tags_secondary` | `arc-matrix.md` distinguishes ● (primary authority) from ○ (touches the arc). Collapsing them into `issue_tags` would destroy that distinction. `issue_tags` = ●, `issue_tags_secondary` = ○ |
| `category` | `A` rulemaking · `B` probable false positive · `C` merits · `X` read but outside the 85-opinion union set (*Fabre*, *Hoang Dinh Duong*) |
| `read_status` | `read` / `unread`. Enforces the "never assert a holding for an unread case" rule at the data layer |

**Counts the file reproduces:** 39 merits cases read (category `C` + `read`), 59 merits clusters, 21 rulemaking clusters, 5 suspected false positives, 2 out-of-corpus. ⚠️ The A-table in `sc-corpus.md` shows **20 rows but 21 clusters** — the October 28, 2021 omnibus restyling has two duplicate cluster entries. The CSV counts clusters.

### ⚠️ Four columns are `unknown` for every row, and one of them should stay that way

- `proposal_outcome`, `fee_disposition` — not recorded per case in `sc-corpus.md`. Fillable by re-reading the coded entries; nothing else blocks it.
- `canon_invoked` — filled for the **six** cases where `sc-corpus.md` records a `Canon:` line (*Willis Shaw*, *Sarkis*, *Campbell*, *Diamond Aircraft*, *Wheaton*, *Coates*, *Trace Elements*); `unknown` elsewhere rather than inferred from the arc-2 tag, which marks that a case *engages* the canon fight, not which side it lands on.
- 🔴 `statute_version` and `rule_version` — **left `unknown` deliberately, and deriving them from `date_filed` would be an error.** Per *Jones Boatyard*, the governing version of § 768.79 is the one in effect **when the cause of action accrued**, not when the opinion issued; § 45.061's trigger is different again (the making of the offer). Filing date is not a proxy. These have to come from each opinion's own recitation of the facts.

---

## 5. Corpus scope — recommendation

Grounded in the real numbers:

- **Full read and code — 85 cases.** Every Florida Supreme Court opinion in the union set. Entirely tractable; this is where the doctrine is actually made.
- **Full code — all conflict-certified DCA cases**, regardless of citation count. These are the pressure points and the reason district attribution mattered.
- **Full code — DCA cases with `citeCount ≥ 1`.** Count not yet measured (see caveat 1).
- **Light code — the remainder**, captured in the database with district, date, and outcome only, so the district-split matrix and timeline stay complete without reading all 901.

---

## Caveats carried into Phase 1

1. **`cited_gt` does not filter.** Passing `cited_gt: 0` returned 901 — identical to unfiltered. Citation-count tiering must be done client-side on retrieved `citeCount` values, not via the API parameter.

2. **901 counts opinions, not cases.** Search `type=o` returns opinions, and `opinion_id` diverges from `cluster_id` in a meaningful share of records (concurrences, dissents, sub-opinions). The true distinct-case count is somewhat below 901. De-duplication on `cluster_id` during retrieval will produce the real figure.

3. **The cascade is validated qualitatively, not yet quantitatively.** Roughly 40 records were probed across all eras and every signal worked where present, but per-tier coverage percentages have not been measured on a random sample. The formal 30-case validation with a measured agreement rate should run as the first task of Phase 3, once retrieval is scripted — it is cheap at that point and expensive now.

---

## Unplanned finding worth keeping

*Mudano* (1989) is not an apportionment or ambiguity case — it holds that § 768.79 does **not** apply where the cause of action accrued before the July 1, 1986 effective date, because § 768.71(2) limits Part III to causes arising on or after that date, and because the statute affects substantive rights and so applies only prospectively.

**Effective-date and retroactivity litigation is a distinct seventh doctrinal arc** dominating the first several years of the case law, and it recurs every time the statute or rule is amended — including right now, with the November 2025 rule amendment. Add it to the Phase 3 arc list.
