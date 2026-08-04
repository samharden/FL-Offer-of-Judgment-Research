# Primary-Source PDF Manifest

Two sets of primary documents sit outside Git, for different reasons. **Archival sources** (§ 1) are excluded because the scans are large and re-retrievable. **Live-case filings** (§ 2) are excluded because they carry counsel's contact details.

---

## 1. Archival sources — legislative track

The PDFs supporting the legislative track are downloadable or reproducible from the official sources below. Local copies belong in `sources/pdfs/`, which is intentionally excluded from Git because the archival scans are large. The manifest, findings, citations, and checksums remain tracked.

| Local filename | Size | Contents and relevant pages | Official source | SHA-256 |
|---|---:|---|---|---|
| `CS-SB-2670-senate-staff-analysis-1990-05-24.pdf` | 399 KB | Seven-page Senate Staff Analysis and Economic Impact Statement for CS/SB 2670, dated May 24, 1990. Exact extraction of source PDF pages 15-21; page 7 contains the consolidation discussion. | [FSU Law, Florida Supreme Court No. 89,623, respondents' answer brief](https://library.law.fsu.edu/Digital-Collections/flsupct/dockets/89623/89623ans.pdf) | `df0c1f1a47ac76d52533ffee8ab22cc4c19f90b2b80e962066a9da545fbf42f7` |
| `ch-86-160-sections-58-61-excerpt.pdf` | 5.7 MB | Ch. 86-160, official session pages 754-756: § 58 creates § 768.79; § 60 creates § 768.81. Exact extraction of source PDF pages 772-774. | [1986 Laws of Florida, vol. I, part 1](https://edocs.dlis.state.fl.us/fldocs/leg/actsflorida/1986/1986V1Pt1.pdf) | `2cff36ecae3dd02ebed6db4235a8702d510b65d74e0cb48d37981d88d7ddfedc` |
| `ch-87-249-laws-of-florida.pdf` | 5.8 MB | Complete three-page act, official session pages 1721-1723. Creates § 45.061 and does not mention § 768.79. Exact extraction of source PDF pages 501-503. | [1987 Laws of Florida, vol. I, part 2](https://edocs.dlis.state.fl.us/fldocs/leg/actsflorida/1987/1987V1Pt2.pdf) | `e60ff0e97e043cdc245e54ea00374c0c0518ce067661b7140f4f473e42dad847` |
| `ch-90-119-laws-of-florida.pdf` | 56.7 MB | Complete ch. 90-119. Enrolled bill identity at source PDF page 400; § 22 at pages 411-412; § 48 at pages 430-432. Exact extraction of source PDF pages 400-433. | [1990 Laws of Florida, vol. I, part 1](https://edocs.dlis.state.fl.us/fldocs/leg/actsflorida/1990/1990V1Pt1.pdf) | `ea5787d5c9f5b0a213528f4b5da5fa5a1b3f2a9beb48b01665b378744bd9a507` |
| `ch-99-225-laws-of-florida.pdf` | 127 KB | Complete 29-page official act. Section 27, beginning on session-law page 20, amends § 768.81; the act does not mention § 768.79. | [Ch. 99-225, Laws of Florida](https://laws.flrules.org/files/Ch_1999-225.pdf) | `4ab1918f1d96b7d0306e8a97dd4bfbdbea6b832b16f38aca42044769ec72f854` |

## 1.1 Local layout

```text
sources/
├── manifest.md          # tracked
└── pdfs/                # ignored
    ├── CS-SB-2670-senate-staff-analysis-1990-05-24.pdf
    ├── ch-86-160-sections-58-61-excerpt.pdf
    ├── ch-87-249-laws-of-florida.pdf
    ├── ch-90-119-laws-of-florida.pdf
    └── ch-99-225-laws-of-florida.pdf
```

## 1.2 Verification

After downloading or recreating the files, verify them from the repository root:

```sh
shasum -a 256 sources/pdfs/*.pdf
```

The checksums above identify the exact copies used for `phase-1-findings.md`. For the four extracted documents, downloading the official source PDF alone will not produce the same checksum; extract the listed source pages in their original order without recompression.


---

## 2. Live-case filings — *Trace Elements, Inc. v. MacKensen*

Florida Supreme Court **No. SC2024-1274**. On review from Fla. 4th DCA No. 4D2023-1707; L.T. No. 312022CC000387 (Indian River County).

⚠️ **These three were tracked in Git until August 4, 2026 and are now excluded.** They are public records, but the two briefs carry **nine email addresses** between them plus firm addresses and phone numbers in their certificates of service. Publishing them to a public repository would put working contact details for named attorneys into a crawlable, indexed location — a materially different exposure from the same document sitting behind a court portal. The history was rewritten to remove them before anything was pushed.

**This creates a real gap, and it should be understood.** The ACIS docket printout is a **point-in-time capture** — it carries a print timestamp of *August 3, 2026, 8:38 a.m.* and shows the docket as it stood while rehearing was pending. That state is **not reproducible**: once rehearing is decided, the live docket will show something different. The local copy is now the only record of it. **Do not delete `Trace Elements/` from disk.**

| Local filename | Size | Contents | SHA-256 |
|---|---:|---|---|
| `Case View - Trace Elements … Florida Appellate Case Information System.pdf` | 1.4 MB | Full ACIS docket, 48 entries, printed **Aug. 3, 2026, 8:38 a.m.**, case status Open. Records the rehearing motion (07/17/2026) and response (07/20/2026) with **no disposing order and no mandate** | `d7f3cd0359cbf3c224f926c91e4c2b6b934c5788f644c2ef8e5b9e2769e71df8` |
| `Motion (SC) - Rehearing.pdf` | 168 KB | Respondents' Motion for Clarification and Rehearing, filed 07/17/2026, 11 pp. | `d7eba0871a99a45a9485df194f1fd279e004885b70431920df25b1e50e411e7a` |
| `Response - Response.pdf` | 230 KB | Petitioner's Response in Opposition, filed 07/20/2026, 24 pp. | `0cb3ff244041cda469e076376ba8e4add45c91f02979abee6c844b0b47e2cbf2` |

### Where to get them again

| Document | Source |
|---|---|
| **Live docket and all filings** | [ACIS — SC2024-1274](https://acis.flcourts.gov/portal/court/68f021c4-6a44-4735-9a76-5360b2e8af13/case/359DF1ED-D650-4B05-8067-811D0695104E) |
| **July 2, 2026 opinion** | [CourtListener](https://www.courtlistener.com/opinion/10883903/trace-elements-inc-v-nadja-mackensen/) · [slip opinion PDF](https://storage.courtlistener.com/pdf/2026/07/02/trace_elements_inc._v._nadja_mackensen.pdf) |
| **Oral argument, Dec. 11, 2025** | [Video](https://www.youtube.com/watch?v=HBBqn7Ya4PU) — the rehearing motion cites 26:02 |
| **Fourth District decision below** | *Mackensen v. Trace Elements, Inc.*, 388 So. 3d 815 (Fla. 4th DCA 2024) |

⚠️ **The ACIS portal is a JavaScript application.** A plain `curl` or `WebFetch` returns nothing, and the `acis-api` docket endpoints 404 on guessed paths. Open it in a browser and print to PDF, which is how the tracked copy was made.

### Local layout

```text
Trace Elements/          # ignored — do not delete; holds the only copy of the Aug. 3 docket state
├── Case View - Trace Elements … .pdf
├── Motion (SC) - Rehearing.pdf
└── Response - Response.pdf
```
