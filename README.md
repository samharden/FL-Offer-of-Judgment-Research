# Offer of Judgment — Fla. Stat. § 768.79 & Fla. R. Civ. P. 1.442

Research project tracking three parallel histories:

1. How Florida courts have treated the offer-of-judgment statute over time
2. How the Legislature has amended the statute
3. How the Supreme Court has amended the implementing rule

Owner: **Sam Harden**. Started August 2026.

The live question driving the work is ***Trace Elements, Inc. v. MacKensen***, No. SC2024-1274 (Fla. July 2, 2026) — 4–3, **rehearing pending and undecided**. Nothing in this repository should be treated as final until that docket is re-pulled.

---

## Where to start

| If you want… | Read |
|---|---|
| Orientation, the thesis, verified facts, tooling gotchas | [`CLAUDE.md`](CLAUDE.md) |
| What remains to be done | [`research-plan.md`](research-plan.md) |
| The case law, coded | [`sc-corpus.md`](sc-corpus.md) |
| The analytical consolidation | [`arc-matrix.md`](arc-matrix.md) |

## File map

| Path | Contents |
|---|---|
| `CLAUDE.md` | Project memory — orientation, thesis, verified facts, working conventions, tooling |
| `research-plan.md` | Plan for remaining work, plus a retrospective on what the original plan got wrong |
| `phase-0-findings.md` | District-attribution cascade, corpus map, coding schema |
| `sc-corpus.md` | The 85 Florida Supreme Court opinions — triage, Tier A/B/C, coded entries, Phase 2 rule track, *Trace Elements* rehearing record |
| `arc-matrix.md` | 39 cases × 10 doctrinal arcs, the Supreme Court alignment matrix by district, the two-track timeline |
| `phase-1-handoff.md` | The legislative-track assignment as handed off (completed; retained as the assignment record) |
| `phase-1-findings.md` | Legislative-track findings and provenance |
| `sources/manifest.md` | Retrieval manifest for primary documents, including official links, page ranges, sizes, and checksums |
| `sources/pdfs/` | Local primary-document copies; intentionally ignored by Git |
| `Trace Elements/` | Primary documents for the live case — ACIS docket, rehearing motion, response in opposition |

---

## Provenance

Work on this project comes from more than one source. Commit history is the record of which is which — each commit message states what produced the content.

| Marker | Meaning |
|---|---|
| `[claude]` | Produced by Claude Opus 5 in Claude Code |
| `[chatgpt]` | Produced by ChatGPT 5.6 Sol, working from a scoped handoff brief |
| `[sam]` | Written or edited directly by Sam Harden |

Keep the prefix on future commits. The distinction matters because verification standards differ by source: anything returned from a handoff is **provisional until checked against the primary document**, and the project's conventions require that check to be visible rather than assumed.

## Working conventions

Carried from `CLAUDE.md`; they apply to anything committed here.

- **Never assert a holding for an unread case.** `sc-corpus.md` tracks read status per case — keep that column honest.
- **Every statutory pin cite carries a year.** Ch. 2022-271 renumbered § 768.79's subsections; a bare subsection reference is ambiguous. See the two-subsection-(6) trap in `CLAUDE.md`.
- **Absolute dates everywhere.** Never "last year" or "recently."
- **Mark confidence.** ✅ verified from a primary source · ⚠️ needs verification · 🔴 live risk.
- **Distinguish what a document says from what a court said it says.** Provenance upgrades are worth recording as such.

## Excluded from version control

`tmp/` holds intermediate retrieval artifacts — full session-law volumes and per-page scans (~300 MB). `sources/pdfs/` holds curated local copies of the primary documents. Both directories are reproducible and excluded from Git; [`sources/manifest.md`](sources/manifest.md) is the tracked retrieval record.

**The test is re-retrievability, not file type.** Archival material — session laws, staff analyses — can be pulled again from a stable official URL, so the manifest suffices. Point-in-time captures cannot: the `Trace Elements/` filings are a dated snapshot of a docket that is still moving, and the ACIS print timestamp is not reproducible. Those three PDFs are tracked deliberately. Manifest what can be re-fetched; commit what cannot.
