# Research Plan — Fla. Stat. § 768.79 and Fla. R. Civ. P. 1.442

**Project:** How Florida courts have treated the offer-of-judgment statute over time, how the Legislature has changed the statute, and how the Supreme Court has changed the implementing rule.

**Originally drafted:** August 2, 2026 · **Rewritten:** August 2, 2026, after Phase 0 and the bulk of Phase 3

> Orientation, thesis, verified facts, and tooling live in [CLAUDE.md](CLAUDE.md). The full corpus and coded entries live in [sc-corpus.md](sc-corpus.md). **This file is the plan for the work that remains.**

---

## What the original plan got wrong

Worth recording, because it changes how the rest should be run.

**1. The phase order was backwards.** The plan treated Phases 1 (legislative) and 2 (rule) as archival research to be done before or alongside the case law. In practice, **the case law contained most of both**:

- *Sarkis* (2003) lays out the entire rule genealogy, 1972 → 1996, in one opinion.
- *Timmons* (1992) and *MX Investments* (1997) give ch. 90-119 **section by section with an effective date** — § 48 (rewrote § 768.79(1), added subsection (6), eff. Oct. 1, 1990) and § 22 (repealed § 45.061 prospectively).
- *Jones Boatyard* (1993) settles which statutory version applies.
- *Lamb* (2005) reveals the *Fabre* origin of rule 1.442(c)(3) via the committee notes.

**Read the case law first; use it to target the archives.** That approach reduced Phase 1 to four questions, all of which were resolved from primary documents on August 3, 2026.

**2. Citation count is the wrong ranking.** The plan ordered reading by `citeCount`. That produced five confirmed misrankings — *Rollins* (121 citations, a PIP setoff case), *D'Angelo* (99, a setoff case), *Aspen* (58), *Wilson v. Salamon* (57), and *Manasse* (77, likely). A **doctrinal-density triage** replaced it and cut the remaining reading by roughly two-thirds at ~73% precision.

**3. The corpus is smaller and cleaner than estimated.** 901 opinions in the union set, but only **56 of the 85 Supreme Court opinions contain "768.79" at all**. Triage before reading.

**4. Trellis never got authorized**, so the trial-court question the plan flagged as most interesting remains unanswered. Still true, still worth doing.

---

## Current state

| Phase | State |
|---|---|
| **0** — scaffolding | ✅ Complete. District-attribution cascade solved; corpus mapped |
| **1** — legislative | ✅ **Complete August 3, 2026.** Four questions resolved from primary documents; see `phase-1-findings.md` |
| **2** — rule | ✅ **Complete (Aug. 3, 2026).** All amendment opinions read; *Fabre* premise verified from the committee note |
| **3** — case law | 85 SC opinions triaged; **40 of ~57 merits cases read**; Tier A complete; 1989–1996 foundation complete |
| **4** — synthesis | Not started. **Now the highest-value work** |

---

## Phase 1 — Legislative track ✅ COMPLETE (August 3, 2026)

The targeted retrievals are complete:

1. ✅ ⭐ **The May 24, 1990 staff analysis was retrieved.** It is a Senate analysis for **CS/SB 2670**; the *White* dissent's `CS/HB 2670` is a miscitation. Page 7 supplies the consolidation discussion.
2. ✅ **Ch. 87-249** created § 45.061 and did not touch § 768.79. Its absence from the § 768.79 credit line is correct.
3. ✅ **Ch. 99-225** did not touch § 768.79. It amended § 768.81 in section 27.
4. ✅ **Ch. 86-160 § 60** created § 768.81; § 58 created § 768.79.

Full findings and provenance are in `phase-1-findings.md`; stable source URLs, page ranges, checksums, and local filenames are in `sources/manifest.md`. Downloaded PDFs live in the Git-ignored `sources/pdfs/` directory.

**Already sourced, no archive needed:** ch. 86-160 (creation), ch. 90-119 §§ 22 and 48, ch. 97-102 (reviser's), ch. 2022-271 (§ 768.79(6), overriding *Gorka*; also renumbered the subsections), ch. 2023-15 § 11 (repealed § 627.428, eff. March 24, 2023).

**Optional:** `fl-lobbyist` on the 2022 bill; the `florida-legislative-analysis` skill on its strike-through/underline text.

---

## Phase 2 — Rule track ✅ COMPLETE (August 3, 2026)

All three outstanding opinions read, plus *Fabre* and the 1996 rewrite. Coded in the Phase 2 section at the end of `sc-corpus.md`.

1. ✅ **550 So. 2d 442 (1989)** — read. Declined constitutionality (confirmed from the opinion itself); proceeded by supersession. ⭐ **New finding:** the 1990 rule expressly allowed offers "by any party or parties," naming "the party or parties," stating "the total amount" — **no apportionment requirement of any kind.**
2. ✅ **112 So. 3d 1209 (2013)** — read. Out-of-cycle, unanimous; (f)(1) cross-reference 1.090(e) → Fla. R. Jud. Admin. 2.514(b).
3. ✅ **Nov. 13, 2025 (SC2025-0045)** — read. Eff. Jan. 1, 2026, unanimous, AOSC22-78 restyling. ⭐ **(c)(3) reopened and re-adopted with only *shall* → *must*; Committee Notes [No Change].**
4. ✅ ⭐⭐ **The *Fabre* origin of (c)(3) is verified from the primary source** — the 1996 committee note at 682 So. 2d 105, 126, verbatim. Pariente's characterization in *Lamb* is exact. Reading *Fabre* itself strengthens the argument considerably (defendant-side fault allocation; the spouse there was an at-fault **nonparty**; and *Fabre* refused to treat "party" as a word of limitation in a companion section of the **same session law** that *Hingson* read restrictively).

**Reactivity typology — the mechanism the project is about, now complete for all eight amendments.** See the table at the end of `sc-corpus.md`. Result: only three of eight amendments were decision-driven and one statute-driven; the rest are housekeeping. **(c)(3) has survived thirty years and four amendment cycles without its substance being revisited once.**

⚠️ **One loose end:** pull the formatted SC2025-0045 slip opinion PDF to resolve the (c)(2)(B) and (c)(2)(F) edits — plain text loses the underline/strikethrough.

---

## Phase 3 — Case law (remaining)

**Reading is largely done.** What remains:

1. **Tier B — 11 cases, light-code.** Spot-check the four high-citation entries first: *Manasse* (77), *Macedo* (44), *Joyce* (33), *Odom* (15).
2. **Tier C — 9 cases, light-code.** None mentions § 768.79. The three pre-statute rule cases (*CU Associates*, *Cheek*, *Fixel*) matter only if Phase 2 needs the 1972–1986 rule history.
3. **Verify the five suspected false positives** and the 1980 rulemaking opinion (391 So. 2d 165). The 1972 entry is confirmed as rule 1.442's origin.
4. **Run the formal 30-case district-attribution validation** when retrieval is scripted — cheap then, expensive now.

**Then the DCA corpus.** ~816 district court opinions remain untouched. Recommendation: **do not read them individually.** Retrieve, apply the four-signal district cascade, code by arc and outcome, and read only conflict-certified cases and those the Supreme Court cites. The Supreme Court corpus already supplies the doctrine; the DCA corpus supplies the **distribution** — which is what the district-split matrix needs.

---

## Phase 4 — Synthesis (now the priority)

The thesis is settled enough to write. Deliverables, in order of value:

1. ✅ **Survey of the regime** — **Markdown** (`memo.md`). ⭐ **Scope corrected August 4, 2026.** Drafted first as an argument about *Trace Elements*, then rewritten as a survey: how offers of judgment work mechanically, the two-track history, the constitutional architecture, all ten arcs, cross-cutting patterns, gaps. *Trace Elements* is one decision inside arc 3.
   - **The framing test for future work:** does this describe how the regime works, or does it argue about one case? The first is the spine.
   - Still to do: a second pass once *Trace Elements* rehearing resolves, and confirmation of `365 So. 3d 353` (*Coates*).
2. ✅ **Two-track timeline** — built, at `visuals/two-track-timeline.html` (also published as an artifact). 35 events, statute vs. Court, three causal loops called out, table view included.
3. **Master case database** — **CSV** (`case-database.csv`). The reusable asset. Schema in `phase-0-findings.md` §4.
4. **District-split matrix** — requires the DCA corpus coded by district.
5. **Practitioner checklist.** Anchor on the *Anderson* / *Audiffred* line: a proposal becomes "joint" when it **speaks for or binds** another party, not merely because another party has claims pending. Include the drafting traps found — rule 1.442(f)(1) excludes Fla. R. Jud. Admin. 2.514(b); a rule 1.090 motion does **not** toll acceptance (*Koppel*); offers may not be aggregated (*Anderson*); dismissal must be **with prejudice** (*MX Investments*).
6. **Live-issues watchlist.** *Trace Elements* rehearing status; whether the Rules Committee takes up the majority's invitation to amend (c)(3); the 2027 session.

---

## Methodology — what actually works

**Triage before reading.** Run `"768.79"` alone against `court=fla` as a control, then per-arc density queries. It matches on vocabulary, so it identifies candidates but cannot separate a holding from a quotation — expect ~73% precision and verify by reading.

**Rank by in-corpus citation, never global `citeCount`.**

**District attribution** uses the four-signal cascade in `phase-0-findings.md` §1. Record which signal fired per case.

**Version every citation.** Per *Jones Boatyard*, the applicable § 768.79 version is the one in effect **when the cause of action accrued**; § 45.061's trigger is **the making of the offer**. Ch. 2022-271 renumbered the subsections, so a bare "(7)(b)" is ambiguous without a year.

**Read dissents separately.** They are distinct sub-opinions (usually majority `opinion_id` + 1) and have repeatedly proved more valuable than the majorities — Polston in *Gorka* became law; Canady in *CCM* supplied the theory behind four other opinions.

**Never assert a holding for an unread case.** `sc-corpus.md` tracks read status per case.

---

## Open decisions

1. **Scope of "courts."** Florida appellate only, or also the Eleventh Circuit and Florida federal district courts applying § 768.79 as substantive law under *Erie*? *Southeast Floating Docks* makes this sharper than it looked: § 768.79 is substantive for **conflict-of-law** purposes too, so the federal cases turn on a question the Court has answered. Roughly doubles Phase 3.
2. **Trellis authorization** for trial-court dockets. Still the only route to testing whether appellate strictness changes trial-court behavior — the most interesting unanswered empirical question here, and nobody has done it.
3. ✅ ~~**Archival depth for Phase 1.**~~ The targeted documentary record is complete; no in-person archive request is presently needed.

---

## Risks

- 🔴 ***Trace Elements* is not final — rehearing is PENDING.** Resolved August 3, 2026 from the ACIS docket (saved in `Trace Elements/`): respondents moved for **clarification and rehearing on 07/17/2026**; petitioner responded in opposition **07/20/2026**; **no order, no mandate**, case status **Open**. This is now a known live risk rather than an unknown one. **Re-pull the docket immediately before any deliverable ships** — and note that a grant of *clarification* alone could narrow the holding without full rehearing.
  - Docket source for re-pulls: `acis.flcourts.gov`, court `68f021c4-6a44-4735-9a76-5360b2e8af13`, case `359df1ed-d650-4b05-8067-811d0695104e`. The portal is a JS app — a plain fetch returns nothing and the `acis-api` docket endpoints 404, so print to PDF from a browser as was done here.
  - ⚠️ **The rehearing motion and the response are not yet in the project folder** — only the Case View docket saved. Get both; the motion frames what the Court is being asked to fix, and if it argues the *Fabre* mismatch or the 2025 restyling, the memo should engage it directly.
- ✅ ~~The *Fabre* origin of (c)(3) is single-sourced~~ — **resolved August 3, 2026.** Verified verbatim from the 1996 committee note, 682 So. 2d 105, 126. No longer a risk.
- ✅ ~~**The 1990 staff analysis has a chamber discrepancy**~~ — resolved from the document itself: Senate, CS/SB 2670. The `CS/HB 2670` reference is a miscitation.
- **DCA volume.** ~816 opinions is tractable only if coded rather than read. Budget accordingly.
