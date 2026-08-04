# Primary-Source PDF Manifest

The PDFs supporting the legislative track are downloadable or reproducible from the official sources below. Local copies belong in `sources/pdfs/`, which is intentionally excluded from Git because the archival scans are large. The manifest, findings, citations, and checksums remain tracked.

| Local filename | Size | Contents and relevant pages | Official source | SHA-256 |
|---|---:|---|---|---|
| `CS-SB-2670-senate-staff-analysis-1990-05-24.pdf` | 399 KB | Seven-page Senate Staff Analysis and Economic Impact Statement for CS/SB 2670, dated May 24, 1990. Exact extraction of source PDF pages 15-21; page 7 contains the consolidation discussion. | [FSU Law, Florida Supreme Court No. 89,623, respondents' answer brief](https://library.law.fsu.edu/Digital-Collections/flsupct/dockets/89623/89623ans.pdf) | `df0c1f1a47ac76d52533ffee8ab22cc4c19f90b2b80e962066a9da545fbf42f7` |
| `ch-86-160-sections-58-61-excerpt.pdf` | 5.7 MB | Ch. 86-160, official session pages 754-756: § 58 creates § 768.79; § 60 creates § 768.81. Exact extraction of source PDF pages 772-774. | [1986 Laws of Florida, vol. I, part 1](https://edocs.dlis.state.fl.us/fldocs/leg/actsflorida/1986/1986V1Pt1.pdf) | `2cff36ecae3dd02ebed6db4235a8702d510b65d74e0cb48d37981d88d7ddfedc` |
| `ch-87-249-laws-of-florida.pdf` | 5.8 MB | Complete three-page act, official session pages 1721-1723. Creates § 45.061 and does not mention § 768.79. Exact extraction of source PDF pages 501-503. | [1987 Laws of Florida, vol. I, part 2](https://edocs.dlis.state.fl.us/fldocs/leg/actsflorida/1987/1987V1Pt2.pdf) | `e60ff0e97e043cdc245e54ea00374c0c0518ce067661b7140f4f473e42dad847` |
| `ch-90-119-laws-of-florida.pdf` | 56.7 MB | Complete ch. 90-119. Enrolled bill identity at source PDF page 400; § 22 at pages 411-412; § 48 at pages 430-432. Exact extraction of source PDF pages 400-433. | [1990 Laws of Florida, vol. I, part 1](https://edocs.dlis.state.fl.us/fldocs/leg/actsflorida/1990/1990V1Pt1.pdf) | `ea5787d5c9f5b0a213528f4b5da5fa5a1b3f2a9beb48b01665b378744bd9a507` |
| `ch-99-225-laws-of-florida.pdf` | 127 KB | Complete 29-page official act. Section 27, beginning on session-law page 20, amends § 768.81; the act does not mention § 768.79. | [Ch. 99-225, Laws of Florida](https://laws.flrules.org/files/Ch_1999-225.pdf) | `4ab1918f1d96b7d0306e8a97dd4bfbdbea6b832b16f38aca42044769ec72f854` |

## Local layout

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

## Verification

After downloading or recreating the files, verify them from the repository root:

```sh
shasum -a 256 sources/pdfs/*.pdf
```

The checksums above identify the exact copies used for `phase-1-findings.md`. For the four extracted documents, downloading the official source PDF alone will not produce the same checksum; extract the listed source pages in their original order without recompression.
