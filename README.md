# Offer of Judgment — Fla. Stat. § 768.79 & Fla. R. Civ. P. 1.442

A research project on Florida's offer-of-judgment regime, tracking three parallel histories:

1. **How Florida courts have treated the statute** over forty years
2. **How the Legislature has amended it** — four times since 1986
3. **How the Supreme Court has amended the implementing rule** — at least eight times since 1972

Owner: **Sam Harden**. Started August 2026.

The regime is split across two instruments by constitutional necessity — the substantive right in the statute, the procedure in the rule — and most of what is interesting about it comes from the two institutions revising each other's work over five decades.

> 🔴 **One live matter affects several statements.** ***Trace Elements, Inc. v. MacKensen***, No. SC2024-1274 (Fla. July 2, 2026), is **not final** — a motion for clarification and rehearing was filed July 17, 2026; no order, no mandate. Re-pull the ACIS docket before relying on the apportionment sections.

## What the deliverable is

[`memo.md`](memo.md) is a **survey of the whole regime** — how offers of judgment work mechanically, and how the statute, the rule, and the case law have revised each other since 1972. Eight parts: the mechanics, the two-track history, the constitutional architecture that splits the regime in two, all ten doctrinal arcs, cross-cutting patterns, open gaps, and its own limits.

⭐ **Scope was corrected on August 4, 2026.** An earlier draft was organised as an argument about *Trace Elements* and the joint-proposal apportionment requirement. That was too narrow — *Trace Elements* is one decision within one of ten arcs. The apportionment analysis survives as the deepest-developed section, but it is now a part of the survey rather than its frame. When adding to this project: **does this describe how the regime works, or does it argue about one case?**

---

## The two legislative strategy folders

**Added August 7, 2026.** Two advocacy planning exercises sit on top of the survey, in [`legislative-strategy-insurer/`](legislative-strategy-insurer/) and [`legislative-strategy-victim/`](legislative-strategy-victim/). Each asks how the Legislature would amend § 768.79 to serve one interest, and whether the result would survive the Florida Supreme Court.

### Why they exist

> Essentially I wanted to experiment with Claude's ability to plan out long-term strategy with multiple unpredictable variables. Certainly planning a strategy that requires understanding the politics between three separate branches of state government is complicated and, even in a one-party majority state, unpredictable. The two scenarios I asked it to plan are narrow, but diametrically opposed: creating a more favorable environment for insurers, and one for victims of intentional torts, using the Offer of Judgment statute as a vehicle, and requiring it to navigate the probabilities of success.
>
> — Sam Harden

**They are deliberately paired and deliberately opposed.** The same statute, the same corpus, and the same three-branch constraint, argued from two chairs that want incompatible things. Reading either alone gives a distorted picture; the point of the exercise is the pair.

### What each one is

| Folder | The chair it argues from | Question |
|---|---|---|
| [`legislative-strategy-insurer/`](legislative-strategy-insurer/) | A medical malpractice **insurer** | How would a carrier amend § 768.79 to improve its own outcomes? |
| [`legislative-strategy-victim/`](legislative-strategy-victim/) | **Victims of intentional torts** | How would the Legislature reduce claimants' fee-shifting exposure? |

Each folder holds a `strategy-memo.md` (the deliverable — levers, constitutional gates, three scenarios with passage and survival odds, coalition, calendar, the case against, and what is unverified) and a `draft-language.md` (working statutory text for every scenario).

⭐ **Two different kinds of thought trace, and they are not interchangeable.** `legislative-strategy-insurer/` holds both; the distinction is the more interesting artifact of the experiment.

| File | What it is |
|---|---|
| `thought-trace-copied-from-claude-code.md` | The **raw reasoning stream**, copied out of the run as it happened. Unstructured, starts mid-thought, interleaved with tool calls. ⚠️ **Partial** — see the two limits below |
| `thought-trace.md` | The **reconstruction** — written afterwards, on request, describing how the memo was built: the moves discarded, the errors caught mid-draft, and where the analysis turned on something unverifiable |

The second is not a cleaned-up copy of the first. It is a **self-report**, produced separately, and it differs from the contemporaneous record. Anyone evaluating what the model actually did should read the raw trace; anyone evaluating what it says it did should read the reconstruction. ⚠️ `legislative-strategy-victim/` has **only the reconstruction** — no raw trace was captured for that run, so the comparison is available on the carrier side only.

⚠️ **Two limits on the raw trace, established by reading it August 8, 2026.**

1. **It stops before drafting starts.** The last line is the model planning the memo's architecture. Everything after that — the actual writing — is unrecorded. So the raw trace covers **research and scenario design only**, and it does **not** independently corroborate the reconstruction's account of the errors caught mid-draft. That part of `thought-trace.md` has no contemporaneous check against it.
2. **The copy is lossy.** At least four points drop text mid-sentence or mid-word — a sentence about equal protection runs straight into `ily impair the constitutional guarantee`, and two tool-call summaries cut off (`—Mc`, `— that`). Treat gaps as copy artifacts, not as the model trailing off.

📌 **The raw trace names a folder that no longer exists, and that is deliberate.** It refers to writing into `legislative-strategy/` — the name both folders were renamed away from on **August 8, 2026**. The reference was **left unedited**: the file is a verbatim record of what the model said while it worked, and editing it to match a later decision would destroy the only property that makes it worth keeping. **Every other file was updated; this one is frozen by design.** Expect the same of any future rename.

✅ **What the comparison does show, on the stretch that is recorded.** Two things the raw trace flagged survived into the deliverable intact: the **November 3, 2026 gubernatorial election** — noted in the trace as an unverifiable input because it has not happened yet — is carried into the memo as *"the highest-variance input"* and repeated in the unverified list; and the instinct to verify the *McCall* and *Kalitan* citations **because this project had previously caught fabricated ones** is recorded in the trace before the check and reflected in the verification table. On the recorded stretch, the self-report and the contemporaneous record agree.

Each memo prices its scenarios twice — **probability of passage** and **probability of surviving the Florida Supreme Court** — because those two variables move independently and often in opposite directions. The clearest illustration is the pair's own structural inversion: on the carrier side the largest ask carries the largest constitutional risk, while on the claimant side the constitutional odds are the highest in either folder and **the entire risk is political**.

### 🔴 How to read them

- ⚠️ **Each folder is one-sided by design.** The survey in [`memo.md`](memo.md) is neutral; these are not. Both memos carry an explicit *case against* section and an explicit *unverified* list, and both state the rule loudly: **this material must not migrate into the survey.**
- ⚠️ **They are planning exercises, not filings and not advice.** Neither has been through the verification pass that gates the survey. Both carry open items that must close before anything is usable — most importantly, **cases cited but not read**. The carrier memo names six (*McCall*, *Kalitan*, *Kluger*, *Echarte*, *Smith*, *Franks*); the project's convention that **a verified citation is not a verified holding** applies with full force, and every proposition drawn from them is marked ⚠️ in place.
- **The odds are estimates, and are labelled as such.** They are the output of the experiment, not a finding of the research project.
- **Neither folder is on the survey's critical path.** Nothing in [`memo.md`](memo.md), [`arc-matrix.md`](arc-matrix.md), or [`case-database.csv`](case-database.csv) depends on either.

Both folders share four open items with each other: re-pulling the *Trace Elements* ACIS docket, and building the empirical predicate from the ~816-opinion district corpus that [`memo.md`](memo.md) Part VIII.E flags. See each folder's own README for the full list.

---

## Status

| Phase | State |
|---|---|
| **0** — scaffolding | ✅ Complete |
| **1** — legislative track | ✅ Complete. All four questions closed from primary documents |
| **2** — rule track | ✅ Complete. All amendment opinions read; the *Fabre* premise verified from the committee note |
| **3** — case law | ✅ Complete **for the memo**. 39 merits opinions read and coded. Tier B (11), Tier C (9), and the ~816-opinion DCA corpus remain unread — see *Scope decisions* below |
| **4** — synthesis | 🚧 In progress. Memo drafted and citation-checked; case database and district-split matrix outstanding |

## Where to start

| If you want… | Read |
|---|---|
| **To actually use the device in a case** | ⭐ [`practice-guide.md`](practice-guide.md) · [HTML](visuals/practice-guide.html) |
| How the regime works, and how it changed | [`memo.md`](memo.md) |
| The history as a visual timeline | [`visuals/two-track-timeline.html`](visuals/two-track-timeline.html) |
| Orientation, verified facts, tooling gotchas | [`CLAUDE.md`](CLAUDE.md) |
| What remains to be done | [`research-plan.md`](research-plan.md) |
| The case law, coded | [`sc-corpus.md`](sc-corpus.md) |
| The analytical consolidation | [`arc-matrix.md`](arc-matrix.md) |
| The corpus as data you can query | [`case-database.csv`](case-database.csv) |
| How a carrier would amend the statute | [`legislative-strategy-insurer/`](legislative-strategy-insurer/) |
| How claimants' advocates would amend it | [`legislative-strategy-victim/`](legislative-strategy-victim/) |

### 💡 Consider reading this in Obsidian

This project is a set of **densely cross-linked Markdown files** — the memo cites the corpus, the corpus cites the arc matrix, the strategy folders cite the parent project, and `CLAUDE.md` is referenced from nearly everything. On GitHub or in a plain editor you follow those links one at a time and lose your place. [Obsidian](https://obsidian.md) is free, reads a plain folder with no import step, and makes the structure navigable:

- **Open the repository folder as a vault.** Nothing needs converting — the files are ordinary Markdown and the links are ordinary relative links, so they resolve as-is.
- **Backlinks** show which files point *at* the one you're reading, which is the fastest way to see what depends on a given finding before you change it.
- **Graph view** makes the shape of the project visible — including that the two strategy folders hang off the survey rather than feeding into it.
- **Search across the vault** is the practical way to use the working conventions: finding every ⚠️ or 🔴 marker, or every mention of a case, in one pass.

Nothing here *requires* Obsidian, and no file depends on it — plain Markdown remains the source of truth, per the deliverable-format decision below. ⚠️ Note that `.obsidian/` is **Git-ignored**, so the vault config is not shared; opening the folder creates your own local one.

## File map

| Path | Contents |
|---|---|
| `memo.md` | **The deliverable.** A survey of the regime in eight parts — mechanics, two-track history, constitutional architecture, all ten doctrinal arcs, cross-cutting patterns, open gaps, limits. Every case hyperlinked |
| `practice-guide.md` | **The practitioner deliverable (Aug. 11, 2026).** The same regime as a working tool: the serve decision, the calendar, joint proposals, an element-by-element drafting checklist, how to attack a proposal served on you, the 25% comparison, and thirteen ranked traps. Every case name hyperlinked |
| `visuals/practice-guide.html` | The practice guide as a standalone page — sidebar contents, light/dark, print stylesheet. **Generated from the Markdown; do not hand-edit** |
| `visuals/two-track-timeline.html` | The two-track history as a standalone page — 35 events, statute vs. Court, with the three causal loops |
| `CLAUDE.md` | Project memory — scope note, verified facts, working conventions, tooling gotchas, and arc 3 developed in depth |
| `research-plan.md` | Plan for remaining work, plus a retrospective on what the original plan got wrong |
| `phase-0-findings.md` | District-attribution cascade, corpus map, coding schema, CSV conventions |
| `sc-corpus.md` | The 85 Florida Supreme Court opinions — triage, Tier A/B/C, coded entries, the Phase 2 rule track, the *Trace Elements* rehearing record, and district decisions read in full |
| `arc-matrix.md` | 39 cases × 10 doctrinal arcs, the Supreme Court alignment matrix by district, the two-track timeline |
| `case-database.csv` | **The reusable asset.** 87 rows × 24 columns — the whole 85-opinion Supreme Court set plus *Fabre* and *Hoang Dinh Duong*, keyed on CourtListener `cluster_id`, with citation, docket, category, read status, and (for the 39 read merits cases) panel, vote, and arc tags. Four columns remain uncoded and are marked `unknown` rather than guessed |
| `legislative-strategy-insurer/` | **Strategy exercise — carrier side.** Strategy memo, draft statutory language, and **both** thought traces — the raw reasoning stream and the after-the-fact reconstruction — for amending § 768.79 in a medical malpractice insurer's favour. One-sided by design; see *The two legislative strategy folders* |
| `legislative-strategy-victim/` | **Strategy exercise — claimant side.** The mirror image: reducing intentional-tort victims' fee-shifting exposure. Memo, draft language, and the reconstruction trace only |
| `phase-1-handoff.md` | The legislative-track assignment as handed off (completed; retained as the assignment record) |
| `phase-1-findings.md` | Legislative-track findings and provenance |
| `LICENSE` | MIT, covering the original work only — see *Licence and scope of it* above |
| `sources/manifest.md` | Retrieval manifest — archival sources (§ 1) and live-case filings (§ 2), with official links and checksums |
| `sources/pdfs/` | Local primary-document copies; Git-ignored by policy |
| `Trace Elements/` | Live-case filings — ACIS docket, rehearing motion, response. **Git-ignored**; see *Excluded from version control* |

---

## Licence and scope of it

The original work in this repository — the analysis, the coding, the memo, the timeline, the research notes — is released under the **MIT Licence**. See [`LICENSE`](LICENSE).

⚠️ **The licence does not, and cannot, cover the third-party material.** Two categories are not Sam Harden's to license:

- **The court filings in `Trace Elements/`** — a docket printout and two briefs authored by counsel for the parties. Filings in Florida appellate proceedings are public records, and this repository reproduces them for research; but authorship and any rights in them rest with their authors, not with this project.
- **Quoted material from judicial opinions and legislative documents** throughout the markdown files. Florida judicial opinions and session laws are public records; the quotations are used for scholarship and commentary.

**Nothing here is legal advice**, and the memo is expressly a research work-product with its limits stated in Part VIII. It describes a regime with a live, undecided matter at its edge.

---

# How research decisions were made

This section exists because the *reasoning behind the path* is not recoverable from the outputs, and several of the choices were counterintuitive or were corrections of earlier mistakes.

## 1. The phase order was inverted — deliberately, after it failed

The original plan treated the legislative and rule tracks as archival research to be done **before** the case law. That was backwards. **The case law turned out to contain most of both:**

- *Sarkis* (2003) lays out the entire rule genealogy, 1972 → 1996, in a single opinion.
- *Timmons* (1992) and *MX Investments* (1997) give ch. 90-119 **section by section with an effective date**.
- *Jones Boatyard* (1993) settles which statutory version applies to a given case.
- *Lamb* (2005) reveals the *Fabre* origin of rule 1.442(c)(3) through the committee notes.

**The rule adopted: read the case law first, then use it to target the archives.** That reduced the legislative track from an open-ended archival project to **four specific questions**, all of which were then answered from primary documents in a single pass.

## 2. Retrieve on statute and rule numbers only — never on doctrinal phrases

Florida's terminology **shifted in 1996**. Pre-1996 opinions say "offer of judgment" or "demand for judgment"; post-1996 they say "proposal for settlement."

Querying `"768.79" + "proposal for settlement"` returns 320 hits whose earliest is **1997** — silently truncating a statute that dates to 1986 and hiding the entire foundational era.

**The rule: retrieve on `"768.79"` and `"1.442"` alone, take the union, de-duplicate on `cluster_id`.** Phrase terms belong in the *coding* layer as era markers, never in the query layer.

Resulting corpus:

| Query | Count |
|---|---|
| `"768.79"` | 776 |
| `"1.442"` | 514 |
| Union | 901 |
| Union, Supreme Court only | **85** |
| Supreme Court opinions containing "768.79" at all | **56** |

## 3. Triage before reading — and the limits of the triage

Reading 85 opinions to find the ~40 that matter is wasteful. Two filters were used:

**The control query.** Only 56 of 85 Supreme Court opinions contain "768.79" at all. Running that one query is the cheapest filter in the project and is **reliable as a negative** — if the string is absent, the case is not about the statute.

**A doctrinal-density matrix** — per-arc phrase searches scored against the control. It achieved roughly **73% precision** on the top tier (8 of 11 spot-checked cases were genuinely load-bearing).

⚠️ **Its documented weakness:** it matches on *vocabulary*, so it cannot distinguish a holding from a quotation. All three misses used the right words while quoting or comparing rather than holding. **Density identifies candidates; only reading distinguishes holding from citation.**

## 4. Citation count was rejected as a ranking

The original plan ordered reading by `citeCount`. That produced **five confirmed misrankings** — *Rollins* (121 citations, actually a PIP setoff case), *D'Angelo* (99, a setoff case), *Aspen* (58), *Wilson v. Salamon* (57), and *Manasse* (77).

Global citation counts measure a case's importance *in general*, not its importance *to this question*. **Rank by citations within the § 768.79 / 1.442 set**, not globally — otherwise the reading queue fills with insurance cases that merely touch the statute.

## 5. All six DCAs collapse into one court identifier

CourtListener assigns every Florida district court of appeal the single id `fladistctapp`. There is no `fla1dca` or `fla4dca`. The docket record does not help either — `dockets.court_id` is also `fladistctapp` and `appeal_from` is null. **That approach was tried and abandoned; do not retry it.**

District attribution therefore runs a **four-signal cascade**, with the signal recorded per case so attribution stays auditable:

| Signal | Method |
|---|---|
| **S1** | `download_url` hostname → `(\d)dca\.flcourts\.gov` |
| **S2** | `docketNumber` → `^(?:Nos?\.\s*)?(\d)D(\d{2}\|\d{4})-` |
| **S3** | HTML header → `District Court of Appeal of Florida,?\s+(First\|Second\|…) District` |
| **S4** | Judge-panel lookup, or manual |

Every coded case carries `district_signal` and `district_confidence`. Detail in [`phase-0-findings.md`](phase-0-findings.md) §1.

## 6. Where reading stopped, and why

**Phase 3 stopped at Tier A** — 39 merits opinions read and coded against ten doctrinal arcs — rather than exhausting the corpus.

The justification is in the arc matrix itself: coding showed the doctrine is carried entirely by cases already read, and the Court's divisions **cluster in a single arc** (joint-proposal apportionment) rather than spreading across the statute. Tier B (11 cases) and Tier C (9 cases, none of which mentions § 768.79 at all) are the low-density tail. Reading them would confirm the shape, not change it.

**Recorded honestly as a judgment, not a completion:** Phase 3 is complete *for the memo* and incomplete *as scoped*. See the completion table in [`sc-corpus.md`](sc-corpus.md).

## 7. The DCA corpus is deliberately not being read

~816 district court opinions remain untouched. **The recommendation is not to read them individually.** Retrieve, apply the district cascade, code by arc and outcome, and read in full only the conflict-certified cases and those the Supreme Court cites.

The reasoning: **the Supreme Court corpus supplies the doctrine; the DCA corpus supplies the distribution.** They answer different questions, and only the second requires volume.

⚠️ **A consequence worth stating loudly:** what currently exists in `arc-matrix.md` is the **Supreme Court's alignment with each district** — how often it approved or rejected each one — *not* a district-split matrix. It is labelled as such in both the matrix and the memo. Do not present it as the districts' own distribution.

## 8. Handing off the legislative track

Phase 1 was handed to a different system (ChatGPT 5.6 Sol) rather than done here. The reasoning:

- **It was separable.** Nothing on the memo's critical path depended on it.
- **It was retrieval, not synthesis** — a different kind of task from doctrinal coding.
- **The tooling here was wrong for it.** LegiScan's Florida coverage begins in **2010**; it cannot see ch. 86-160, 87-249, 90-119, or 97-102. Everything known about the pre-2010 record had been reconstructed second-hand from opinions.

The brief ([`phase-1-handoff.md`](phase-1-handoff.md)) was written to be answerable with no project context, and imposed one rule that mattered: **documents, not summaries.** A 1990 staff analysis is exactly the kind of source that is hard to verify and easy to describe plausibly without having seen. A *documented negative* was named as a successful outcome, to remove any pressure to produce something affirmative.

It worked. All four questions came back closed with primary documents, and the return also declined to adopt a premise the brief had asserted — recorded as stated.

## 9. Scope decisions still open

| Question | Status |
|---|---|
| Florida appellate only, or also 11th Circuit / Florida federal courts applying § 768.79 under *Erie*? | **Open.** Leaning Florida-only: *Southeast Floating Docks* already answers the governing question, so federal cases would roughly double Phase 3 for confirmation rather than new doctrine |
| Authorize Trellis for trial-court dockets? | **Open.** Worth doing as a separate empirical piece; not a prerequisite for anything |

## 10. Deliverable formats — plain text

**Decision recorded August 4, 2026.** The memo is Markdown; the case database will be CSV. Neither ties the project to Office formats, and both diff cleanly in Git — which matters for a document whose provenance is the point. Convert to `.docx` at the end if a recipient needs it, but the source of truth stays plain text. CSV serialisation conventions are in [`phase-0-findings.md`](phase-0-findings.md) §4.

## 11. Which source documents go in Git

**Two tests, in order.**

**First — does it contain contact details for people outside this project?** If so it stays out of Git regardless of provenance. The three `Trace Elements/` filings were tracked until August 4, 2026 and are now excluded on this ground: the two briefs carry nine email addresses plus firm addresses and phone numbers in their certificates of service. They are public records, but publishing them to a crawlable, indexed repository is a different exposure from the same document behind a court portal. History was rewritten to remove the blobs before anything was pushed.

**Second — is it re-retrievable?** Archival material like session laws and staff analyses can be pulled again from a stable official URL, so [`sources/manifest.md`](sources/manifest.md) suffices and the bytes stay out.

🔴 **Do not delete `Trace Elements/` from disk.** The ACIS docket printout carries a timestamp of **August 3, 2026, 8:38 a.m.** and shows the docket while rehearing was pending. That state is not reproducible — once rehearing is decided, the live docket shows something else — and the local copy is now the only record of it. Checksums and retrieval routes are in [`sources/manifest.md`](sources/manifest.md) § 2.

### Getting the live-case documents

| Document | Source |
|---|---|
| Live docket and all filings | [ACIS — SC2024-1274](https://acis.flcourts.gov/portal/court/68f021c4-6a44-4735-9a76-5360b2e8af13/case/359DF1ED-D650-4B05-8067-811D0695104E) |
| July 2, 2026 opinion | [CourtListener](https://www.courtlistener.com/opinion/10883903/trace-elements-inc-v-nadja-mackensen/) · [slip opinion PDF](https://storage.courtlistener.com/pdf/2026/07/02/trace_elements_inc._v._nadja_mackensen.pdf) |
| Oral argument, Dec. 11, 2025 | [Video](https://www.youtube.com/watch?v=HBBqn7Ya4PU) |
| Fourth District decision below | *Mackensen v. Trace Elements, Inc.*, 388 So. 3d 815 (Fla. 4th DCA 2024) |

⚠️ ACIS is a JavaScript application — a plain fetch returns nothing and the guessed API endpoints 404. Open it in a browser and print to PDF.

**Manifest what can be re-fetched; commit what cannot.**

`tmp/` holds ~300 MB of intermediate retrieval artifacts — full session-law volumes and per-page scans — and is excluded. Five source PDFs were briefly committed before this policy existed; `main` was rewritten to remove them from history before any remote was added.

---

# Corrections that changed the analysis

Recorded because a research file that only shows conclusions hides its own reliability. Each of these was believed, written down, and then overturned by reading a primary source.

| Was recorded as | Actually | Caught by |
|---|---|---|
| The 1989 rule opinion held §§ 768.79 and 45.061 unconstitutional | It **expressly declined** to reach constitutionality and proceeded by supersession | The original error came from the *trial court's* characterization quoted in *TGI Friday's*; corrected against *Sarkis*, *Timmons*, then the opinion itself |
| *Gorka* is an apportionment case | It is a **conditions** case — the proposal there *was* fully apportioned, $12,500 to each plaintiff | Reading Polston, J.'s dissent, which reproduces the actual proposal |
| *Kuhajda* inverted the strict-construction pendulum | It is a **narrow carve-out**, unanimous in result, that does not reject the canon at all | Reading *Kuhajda* rather than inferring it from later citations |
| Canady's 2015 dissents share a merits theory | Both are **purely jurisdictional**; he reaches no merits question in either | Reading the dissents |
| The Legislature overrode *Gorka* | § 768.79(6) is a **carve-out for property insurers in contract actions**, not a repeal. *Gorka* stands everywhere else | Pulling the statute text directly |
| The *Fabre* origin of (c)(3) was single-sourced from a concurrence | Confirmed **verbatim** from the 1996 committee note itself | Reading 682 So. 2d 105, 126 |
| 40 merits cases read | **39.** *Fabre* was read but sits outside the merits corpus | Counting the list while building the arc matrix |
| History had been rewritten to drop 68 MB of PDFs | It had **not** — the files were removed going forward, leaving the blobs reachable from `main` | Checking `git ls-tree` against the claim in the policy note |

🔴 **And one that no amount of reading would have caught.** During the citation-verification pass, two reporter citations — `351 So. 3d 1080` for *Suarez Trucking* and `322 So. 3d 32` for *CCM Condominium* — were **fabricated**. The project records both cases by docket number only; the cites appear nowhere in these files and were generated when assembling the checker input. Neither is in the memo. Logged in the memo's appendix rather than quietly dropped, because it is the exact failure this project's verification convention exists to catch, and it survived until a database was asked.

**The general lesson, which the conventions below encode:** a citation that resolves to a real case is not the same as a citation that is correct, and neither is the same as a pin cite that says what you think it says.

---

# Provenance

Work here comes from more than one source. **Commit history is the record** — every commit message states what produced the content.

| Marker | Meaning |
|---|---|
| `[claude]` | Produced by Claude Opus 5 in Claude Code |
| `[chatgpt]` | Produced by ChatGPT 5.6 Sol, working from a scoped handoff brief |
| `[sam]` | Written or edited directly by Sam Harden |

Keep the prefix on future commits. The distinction matters because **verification standards differ by source**: anything returned from a handoff is provisional until checked against the primary document, and the check must be visible rather than assumed.

# Working conventions

Carried from [`CLAUDE.md`](CLAUDE.md); they apply to anything committed here.

- **Never assert a holding for an unread case.** `sc-corpus.md` tracks read status per case — keep that column honest. A *half-read* case is where errors actually enter.
- **Every statutory pin cite carries a year.** Ch. 2022-271 renumbered § 768.79's subsections, so a bare subsection reference is ambiguous. 🔴 In particular there are **two different subsection (6)s** — see the trap note in `CLAUDE.md`.
- **Absolute dates everywhere.** Never "last year" or "recently."
- **Mark confidence.** ✅ verified from a primary source · ⚠️ needs verification · 🔴 live risk.
- **Distinguish what a document says from what a court said it says.** Most of what is "known" about ch. 90-119 came from opinions describing it; getting the session law itself is a provenance upgrade and should be recorded as one.
- **Verify every citation before anything ships** — and record what the verification could *not* establish, not only what it confirmed.

# Known limits

- 🔴 ***Trace Elements* is not final.** Re-pull the docket before circulating anything.
- ✅ `365 So. 3d 353` (*Coates*) — **verified August 4, 2026** from ***Trace Elements*'s own citation** of it ("365 So. 3d 353, 355"). The slip opinion was also retrieved from the Florida Supreme Court and is manifested in `sources/manifest.md` § 3. No unverified reporter citations remain in the memo.
- ⚠️ *Ramos*, *Furen*, and *Watkins v. Corbett* are **unread** and are cited in the memo as such.
- ⚠️ The ~816 DCA opinions are untouched. District figures are the Supreme Court's alignment, not a district split.
- ⚠️ Tier B (11) and Tier C (9) Supreme Court cases are unread, which bounds any claim that a proposition appears nowhere else in the corpus.
- ⚠️ **The two strategy folders have not been through this project's verification pass.** They cite cases they have not read (marked ⚠️ in place), and their passage and survival odds are estimates. They are advocacy planning exercises kept separate from the survey — see *The two legislative strategy folders*.
