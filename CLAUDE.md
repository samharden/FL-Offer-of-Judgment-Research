# CLAUDE.md — Project Memory

## What this project is

A research project on **Fla. Stat. § 768.79** (offer of judgment / demand for judgment) and **Fla. R. Civ. P. 1.442** (proposals for settlement), covering three tracks:

1. How Florida courts have treated the statute over time
2. How the Legislature has amended the statute over time
3. How the Supreme Court has amended the implementing rule over time

Owner: Sam Harden. Working directory: `/Users/samharden/Claudeo/OoJ`. **Git repo since August 3, 2026** — see `README.md`. Commits carry a provenance prefix: `[claude]`, `[chatgpt]`, or `[sam]`. Keep it.

## Files

| File | Contents |
|---|---|
| `research-plan.md` | Plan for the *remaining* work, plus a retrospective on what the original plan got wrong. Rewritten Aug 2, updated Aug 3 |
| `phase-0-findings.md` | Phase 0 — district-attribution cascade, corpus map, coding schema, caveats |
| `sc-corpus.md` | The 85 Florida Supreme Court opinions: triage, Tier A/B/C split, coded entries. **Also holds the completed Phase 2 rule-track section and the *Trace Elements* rehearing record** |
| `arc-matrix.md` | **Phase 3 consolidation (Aug 3)** — 39 cases × 10 arcs, the Supreme Court alignment matrix by district, and the two-track timeline |
| `phase-1-handoff.md` | **Self-contained brief for the legislative track**, written for an outside collaborator. Four questions, the traps, sources, deliverable standards |
| `phase-1-findings.md` | **Completed legislative-track findings.** Resolves all four handoff questions and links the retrieved primary PDFs |
| `Trace Elements/` | Primary documents for the live case — ACIS docket (printed Aug. 3, 2026), rehearing motion, response in opposition |
| `CLAUDE.md` | This file — orientation, thesis, verified facts, tooling |

## Git and source-artifact policy

**Decision recorded August 3, 2026:** archival source PDFs do not belong in Git. Local copies live in the Git-ignored `sources/pdfs/` directory; `sources/manifest.md` is the tracked record and must preserve each filename, official retrieval URL, relevant source pages, file size, and SHA-256 checksum. New source PDFs should follow the same pattern.

The five Phase 1 PDFs were briefly committed under `output/pdf/` before this policy was adopted. Before any remote was added, `main` was rewritten to remove that path from every commit so those binary objects would not be included in a future push. Do not re-add the PDFs or recreate the pre-rewrite history on a remote. The local copies remain available and reproducible from the manifest.

## Status — August 3, 2026

| Phase | State |
|---|---|
| **0** — scaffolding | ✅ Complete |
| **1** — legislative track | ✅ **Complete.** Chs. 87-249 and 99-225 resolved; May 24, 1990 CS/SB 2670 Senate staff analysis retrieved; ch. 86-160 § 60 verified |
| **2** — rule track | ✅ **Complete.** All amendment opinions read: 550 So. 2d 442 (1989), 682 So. 2d 105 (1996), 112 So. 3d 1209 (2013), SC2025-0045 (Nov. 13, 2025). *Fabre* origin of (c)(3) **verified from the committee note itself**. Coded in `sc-corpus.md` |
| **3** — case law | 85 SC opinions triaged. **39 of ~57 merits cases read** (the "40" figure was off by one — see `arc-matrix.md`), plus the separate dissents in *Gorka*, *Pratt*, *Audiffred*. **Tier A complete. 1989–1996 foundation complete. ✅ All 39 coded against the ten arcs, Aug. 3.** Remaining: Tier B (11), Tier C (9), and the DCA corpus |
| **4** — synthesis | **Started Aug. 3.** Arc matrix, Supreme Court alignment matrix, and two-track timeline built in `arc-matrix.md`. **Next: draft the memo** |

**Merits cases read (40):** *Unicare*, *Aspen*, *Leapai*, *Timmons*, *Jones Boatyard*, *TGI Friday's*, *Hannah*, *Knealing*, *Gulliver Academy*, *MX Investments*, *MGR Equipment*, *Rollins*, *Hingson*, *White v. Steak & Ale*, *Willis Shaw*, *Sarkis*, *D'Angelo*, *Lamb*, *Saia*, *Nichols*, *Campbell*, *Frosti*, *Massey*, *Gorka*, *Southeast Floating Docks*, *Shands*, *Diamond Aircraft*, *Advanced Chiropractic*, *Pratt*, *Audiffred*, *Anderson*, *Kuhajda*, *Koppel*, *Allen v. Nunez*, *Wheaton*, *CCM Condominium*, *Suarez Trucking*, *Coates*, *Trace Elements*.

**Also read, outside the merits corpus:** the four rule-amendment opinions (550 So. 2d 442 · 682 So. 2d 105 · 112 So. 3d 1209 · SC2025-0045); ***Fabre v. Marin***, 623 So. 2d 1182 (Fla. 1993); the *Trace Elements* rehearing motion and response; the ACIS docket. Partially read: *Hoang Dinh Duong v. Ziadie* (apportionment passage only).

### Two scoping decisions still open

1. Florida appellate only, or also 11th Circuit / Florida federal district courts applying § 768.79 under *Erie*?
2. Authorize Trellis for trial-court dockets?

---

# THE THESIS

*Trace Elements* (2026) **is** doctrinally faithful to *Kuhajda* — rule 1.442(c)(3) does implement what *Hingson* and *Gorka* say § 768.79 requires. The vulnerability is not inconsistency with *Kuhajda*. It is that **the premise *Trace Elements* inherits is the weakest link in a chain that has been repudiated at every point where anyone else got a word.**

## 1. The apportionment line rests on one contested inference

- ***Hingson* (2002)** derived apportionment from the singular "party" in § 768.79(2)(b) in **two hedged sentences** ("this, we believe"), **4–3**, over Harding, J.'s dissent citing **§ 1.01(1), Fla. Stat.** — the Legislature's own directive that "[t]he singular includes the plural and vice versa" — and against **three of the four** DCAs then to have ruled. **Never revisited.**
- Posture matters: *Hingson* involved a **pre-1997 offer** under the old rule 1.442, which read only "Parties shall comply with the procedure set forth in section 768.79." The apportionment language of current (c)(3) **did not exist**. The Court had to derive it from the statute alone.
- ***Audiffred* (2015)** repeats the same 1-versus-3 district alignment.

## 2. The rule provision was built for a different job

✅ **VERIFIED August 3, 2026 against both primary sources.** The 1996 committee note, **682 So. 2d 105, 126**, verbatim:

> "**The provision which requires that a joint proposal state the amount and terms attributable to each party is in order to conform with *Fabre v. Marin*, 623 So.2d 1182 (Fla.1993).**"

Pariente, C.J., wrote in 2005 that the Court's reading "has broadened the reach of the rule **beyond *Fabre*** so that **a joint offer to a husband and wife is no longer authorized**." Her characterization is exact. The point no longer depends on a concurrence.

***Trace Elements* is a husband-and-wife case.** The objection is 21 years old and came from the Chief Justice. **Four spousal casualties now: *Hingson* (2002), *D'Angelo* (2003), *Audiffred* (2015), *Trace Elements* (2026)** — and *Hingson*'s disapproved case, *Herzog*, makes five sets of spouses.

**Reading *Fabre* itself makes the mismatch worse, three ways:**

1. ***Fabre* is a defendant-side fault-allocation case.** § 768.81(3); judgment against each party by percentage of fault, computed against **all participants including nonparties**. It says nothing about co-plaintiffs, lump-sum demands, or settlement mechanics.
2. ⭐ **The spouse in *Fabre* is on the other side of the "v."** Mr. Marin was the at-fault **nonparty** driver, unreachable because of interspousal immunity; the jury put him at 50%. In *Hingson*, *D'Angelo*, *Audiffred*, and *Trace Elements* the spouses are **co-claimants with a unified claim and no fault to allocate**. The provision is being applied to the mirror image of the situation that produced it.
3. ⭐⭐ **Same word, same session law, opposite constructions.** *Fabre* construes "party" in § 768.81(3); *Hingson* construes "party" in § 768.79(2)(b). **Both sections come from ch. 86-160: § 768.79 was created by § 58 and § 768.81 by § 60.** *Fabre* held "party" is **"not intended as a word of limitation"** — "[h]ad the legislature intended … it would have so stated." *Hingson* made the singular "party" precisely a word of limitation. ✅ Confirmed from the primary session law August 3, 2026.

### ✅ The administrability counter-argument — run to ground August 3, 2026, and it fails

Petitioner's rehearing response leaned on *Hoang Dinh Duong v. Ziadie*, 153 So. 3d 354, 358–60 (Fla. 4th DCA 2014), which calls enabling the fee determination "**the other main purpose of the apportionment requirement**." If (c)(3) independently served that purpose, "built for a different job" would be incomplete. **It does not.** Five findings:

1. ⭐ **The rationale exists in this Court exactly once — and it is the sentence immediately before the "this, we believe" sentence.** *Hingson*, 808 So. 2d at 199, in full:
   > "We agree with the district court in *C & S* that '[t]o further the statute's goal, each party who receive[s] an offer of settlement is entitled … to evaluate the offer as it pertains to him or her.' **Otherwise, in many cases, it would be impossible for the trial court to determine the amount attributable to each party in order to make a further determination of whether the judgment against only one of the parties was at least twenty-five percent more or less than the offer** (depending on which party made the offer). Moreover, the plain language of section 768.79 supports the *C & S* court's holding. In subsection (2)(b), the statute refers to 'party' in the singular. **This, we believe,** indicates the Legislature's intent that an offer specify the amount attributable to each individual party."

   It is not an independent purpose. It is **the same contested passage, in the same 4–3 opinion**, that the whole line already rests on. *Hoang Dinh Duong* cites *Hingson* at 199 for it.
2. ⭐⭐ **It is about the *statute*, not (c)(3).** *Hingson* construed § 768.79(2)(b) and the pre-1997 rule, which had no apportionment language. It is not evidence of what rule 1.442(c)(3)'s drafters were doing. **The only direct evidence of that remains the 1996 committee note, and it says *Fabre*. The argument is undamaged.**
3. **No later decision of this Court uses it.** *Willis Shaw*, *Gorka*, *Pratt*, *Audiffred*, and ***Trace Elements* itself contain the phrase "twenty-five percent" zero times.** *Lamb* repeats the passage only by block-quoting *Hingson*. *Trace Elements* cites *Hingson* at 199 **only** for the independent-evaluation half.
4. ⭐⭐⭐ **Harding's dissent already answered it — and *Hingson*'s own facts refute it.** "Rather than worry about what may happen 'in many cases,' it is more appropriate to focus on the facts of this case. The jury returned a verdict in favor of the Defendant, resulting in the Plaintiffs receiving nothing. **There is no question that the judgment was at least twenty-five percent less than the amount of Allstate's offer, regardless of its nonallocation.**" **In the very case that generated the administrability rationale, administrability was not a problem.**
5. ⭐⭐ ***Hingson*'s own worked example (n.3) is a separable-claims case.** K-Mart offered the Herzogs $20,001 jointly; judgments came back **$8,601 for Mrs. Herzog and $3,750 for Mr. Herzog** — two different numbers — and only then is it "not necessarily clear" whether the 25% test was met. The illustration works *because the spouses had distinct judgments*. In a unified-claim case there is one judgment and the math is trivial — as **petitioner's own rehearing response demonstrates**, computing half of the $41,273.70 verdict against a hypothetical $5,000 share. **Petitioner's response inadvertently proves the administrability rationale has no application to a unified claim.**

**Net: thesis point 2 stands as written and gains a limb.** The 4th DCA's "other main purpose" is a district-court gloss on one hedged sentence, from a 4–3 opinion, construing a different instrument, in a case whose own facts did not require it.

⭐ **And the 1990 rule text cuts the same way.** The rule immediately preceding the modern one (550 So. 2d 442, adopted eff. Jan. 1, 1990) provided that an offer "**may be made by any party or parties**," must "name the **party or parties** making the offer and the **party or parties** to whom the offer is made," must "**settle all pending claims**," and must state "the **total amount** of the offer." **Multi-party offers, in the plural, as a single total, with no apportionment requirement.** Apportionment enters the rule only in 1996, and only for the *Fabre* reason.

## 3. Every extension has been repudiated by whoever got the next word

| Case | Repudiated by |
|---|---|
| *Lamb* (2005) | The Court's **own rule amendment**, 52 So. 3d 579, 588 (Fla. 2010), adopting (c)(4) |
| *Gorka* (2010) | The **Legislature**, ch. 2022-271 § 768.79(6); rule conformed, 345 So. 3d 845 (Fla. 2022) — ⚠️ **but narrowly; see the correction below** |
| *Trace Elements* (2026) | Invites the same treatment, expressly citing the post-*Lamb* amendment as its model |

### ⚠️ CORRECTION (August 3, 2026) — the *Gorka* override is much narrower than recorded

Pulled from the statute directly. **§ 768.79(6) reads in its entirety:**

> "For a breach of contract action, a **property insurer** may make a joint offer of judgment or settlement that is conditioned on the mutual acceptance of all the joint offerees."

*Gorka* invalidated a joint proposal conditioned on mutual acceptance. Subsection (6) authorizes exactly that — **but only for property insurers, and only in breach-of-contract actions.** It is a **carve-out, not a repeal.** The earlier note here implied the Legislature overrode *Gorka* generally; it did not.

**The thesis survives, but state it precisely:** the Legislature reached in and disapproved *Gorka*'s rule for the one industry that complained loudest, leaving the holding standing everywhere else. That is still repudiation-by-whoever-got-the-next-word, and arguably a sharper illustration — the fix was **lobbied, narrow, and industry-specific** rather than principled. But do not write that *Gorka* was legislatively overruled.

⚠️ Petitioner's rehearing response describes (6) as "relaxing the **apportionment** requirement in property insurance breach of contract cases." That is also imprecise — (6) addresses **conditional/mutual acceptance**, not apportionment. Do not adopt that characterization.

✅ **Subsection numbering post-2022 — now resolved from the statute.** (1) entitlement; (2) offer requirements; (3) service and filing; (4) acceptance; (5) withdrawal; **(6) property-insurer conditional joint offers (new in 2022)**; **(7) the post-judgment cost-and-fee determination — the 25% math**; **(8) good faith and the reasonableness factors, with the factors at (8)(b)**. This confirms *Coates*'s citations and the mapping from the pre-2022 numbering: old (6) → new (7), old (7)(a)–(b) → new (8)(a)–(b).

✅ **Credit line re-verified:** s. 58, ch. 86-160; s. 48, ch. 90-119; s. 1175, ch. 97-102; s. 24, ch. 2022-271. **Ch. 87-249 is correctly absent:** it created § 45.061 and did not touch § 768.79. See `phase-1-findings.md`.

**And the Court has already run this loop once:** in **2003** the Rules Committee proposed excusing apportionment for vicariously liable parties; the Court **refused**, citing *Willis Shaw* (858 So. 2d 1013, 1014–15). In **2005** *Lamb* created exactly that problem over three justices' written objections. In **2010** the Court adopted essentially the committee's original proposal.

## 4. The pillars are bare or fractured majorities

*Hingson* 4–3 · *Gorka* 4–3 · *Pratt* / *Audiffred* 5–2 · *Allen v. Nunez* 4–3 · *Trace Elements* 4–3. *Lamb* was unanimous in result but **three justices objected in writing**.

## 5. ⭐ The Court has diagnosed itself

Polston, J., dissenting in ***Allen v. Nunez*** (2018), **joined by Canady, C.J., and Lawson, J.**:

> this Court's jurisprudence "**in this area of the law seems inconsistently applied and unpredictable**"

Not an advocate's characterization. **Lead the memo's diagnostic section with it.** The majority's answer (n.2) does not dispute the inconsistency — only what to do about it.

---

# INTERPRETIVE METHOD

## *Coates* undercuts the line that cites it

*Trace Elements* borrows *Coates*'s "**penalty statute**" label to justify strict enforcement. But *Coates* (2023) **never invokes the derogation canon**. Its declared method is the **supremacy-of-the-text principle** (*Levy*, *Page*) and "**we do not add words to a statute in the guise of interpreting it**" (*Statler*).

- *Hingson* **added** an apportionment requirement to "name the party making it."
- *Gorka* **added** an independent-acceptance requirement it conceded precedent only "**inherently requires**."

**The modern Court's textualism is in tension with the apportionment line.** This is the strongest available argument that *Trace Elements* is vulnerable — it uses the current Court's own stated method.

## ⚠️ Strict construction is NOT inherently pro-offeree

Two confirmed instances where textual strictness **saves** a fee award:
- ***Anderson* (2016)** — separate offers may not be **aggregated**: "cannot be tolerated under a strict construction."
- ***Suarez Trucking* (2022)** — refuses to import a mirror-image "**rule of regurgitation**" into acceptance.

The canon cuts against whichever side asks the Court to read something **into** the text. **The Court refuses additions when they would defeat a fee award as readily as it makes them when they would.** *That inconsistency, not strictness itself, is the memo's real target.*

## ⚠️ *Koppel* weakens the rule-1.010 argument

Bell (*Campbell* 2007) and Sasso (*Trace Elements* 2026) both argue **rule 1.010** should govern instead of the derogation canon. ***Koppel* (2018), unanimous**, forecloses that at the threshold: rule 1.010's "just, speedy, and inexpensive" directive applies "**only if a rule needs interpretation** — [h]ere, the language is clear and unambiguous."

Since *Trace Elements* treats (c)(3) as unambiguous, **engage *Koppel* rather than presenting rule 1.010 as a clean answer.** Note it is consistent with *Coates*: no ambiguity, no canon of any kind.

## The constitutional test — *Knealing* (1996)

A statute in this field survives art. V, § 2(a) **only if it contains a substantive fee-authorizing provision**. §§ 45.061 and 768.79 survived (*Leapai*, *Timmons*); § 44.102(6)'s mediation timing rules, being purely procedural, did not. The cleanest statement of the substance/procedure line in the corpus. The **test itself** comes from *Massey v. David* (2008), quoting *Haven Fed. Sav. & Loan v. Kirian*.

### ⭐ The same axis, pointed the other way — a rule that *enlarges* a substantive right

From respondents' *Trace Elements* rehearing motion, and worth taking seriously on its own: ***Ramos v. State***, 505 So. 2d 418, 421 (Fla. 1987) (citing ***State v. Furen***, 118 So. 2d 6 (Fla. 1960)) — "substantive rights conferred by law can neither be **diminished nor enlarged** by procedural rules adopted by this Court."

The argument: strict compliance with (c)(3) can **expand** the § 768.79 right, because splitting a joint offer lowers each offeror's comparator and makes the 25% threshold easier to beat. Every substance/procedure argument in this corpus runs the other direction — that the rule *contracts* the statutory right. This one is the mirror image, and it pairs with the confirmed finding that **strict construction is not inherently pro-offeree** (below). ⚠️ *Ramos* and *Furen* are unread; both are outside the 768.79 corpus.

## ***Wheaton* remains unreconciled**

Its alternative holding applies the substantive-compliance test to a **different rule set** (2.516) — broader than anything *Kuhajda* did — and the *Trace Elements* majority never mentions it.

---

# SEPARATE-OPINION GENEALOGIES

Four documented threads from separate writing into doctrine.

| Thread | Path |
|---|---|
| **Pro-strict** | **Wells**, *TGI Friday's* separate opinion (1995) → his ***Willis Shaw*** majority (2003). Later cases cite *TGI Friday's* at **615** — a page inside his 1995 separate opinion — as the anchor |
| **Anti-canon** | **Bell**, *Campbell* concurring in result (2007), invoking rule 1.010 and quoting Farmer, J., below → cited in ***Trace Elements*** (2026) |
| **Distinguishability** | **Lewis**, *Lamb* concurring in result (2005): the result is "**purely the product of the technical language of the rule, not logic or proper legal reasoning**" → Sasso's 2026 dissent |
| **Precedent scope** | **Canady**, *State v. Yule* (Fla. 2d DCA 2005) (specially concurring) → *Pedroza v. State* (Fla. 2020) → **cited in Sasso's *Trace Elements* dissent**. The 2026 dissent rests on a definition of "holding" Canady wrote as a district judge |

## Canady's unifying theory

One objection across a decade: **the Court treats broad statements as holdings and extends them past what was actually decided.**

- **Jurisdictionally** — *Pratt* and *Audiffred* dissents (2015) are **purely jurisdictional**; he reaches no merits question
- **On the merits** — ***Kuhajda*** (2016), where conflict was properly certified and he had a vehicle
- **As explicit theory** — ***CCM Condominium* dissent (2021)**, quoting Garner's *The Law of Judicial Precedent*: "assumptions a court uses to reach a particular result do not themselves create a new precedent"

⭐ In *CCM* he disclaims the reach of ***his own*** *Shands* opinion. Reading *Shands* confirms he was right — it never discusses post-offer costs or interest.

## The Canady–Polston bloc

Dissented on **jurisdictional** grounds in *Pratt* (2015), *Audiffred* (2015), *Allen* (2018); concurred **in result only** in *Anderson* (2016). Four consecutive refusals to join this line's reasoning, always on the same ground.

## Bench composition

*Coates* (2023) — Muñiz, C.J., Canady, Couriel, Francis, Grosshans, Labarga; **Sasso did not participate**.
**SC2025-0045 (Nov. 13, 2025)** — Muñiz, C.J., Canady, Labarga, Couriel, Grosshans, Francis, Sasso. **Unanimous.**
*Trace Elements* (2026) — Muñiz writes; Couriel, C.J., Labarga, Grosshans concur; **Sasso, Francis, Tanenbaum dissent**.
**Francis moved from the *Coates* majority to the *Trace Elements* dissent.**
⭐ **The bench turned over between the 2025 rule amendment and *Trace Elements*:** Canady is gone, **Tanenbaum** has joined, and the chief justiceship passed **Muñiz → Couriel** — with Muñiz, no longer chief, writing the majority. Every justice who joined the unanimous November 2025 restyling of (c)(3) except Canady was still sitting in July 2026, and **three of them dissented** on what it means. ⚠️ Verify against the Court's roster before relying on this.

⚠️ **Labarga tension to check:** dissents in *Suarez Trucking* (2022) arguing for a common-law overlay, then joins the *Trace Elements* majority applying rigid rule enforcement. Verify before characterizing his position.

---

# QUOTABLE MATERIAL

- ***Gorka***, 36 So. 3d at 650 — admission against interest: the sanction was meant "to reduce litigation costs and conserve judicial resources," but "[t]he effect, however, **has been in sharp contrast to the intended outcome** because the statute and rule have seemingly increased litigation."
- ***Allen v. Nunez*** (Polston, J., dissenting, with Canady and Lawson) — "**inconsistently applied and unpredictable**."
- ***Unicare*** (1989) — the purposive pole, and its **origin**: rule 1.442 "was implemented **solely to encourage settlements in order to eliminate trials if possible**," intended "to terminate all claims, end disputes, and obviate the need for further intervention of the judicial process." Quoted thereafter in *Segall*, *Gorka*, Pariente's *Lamb* and *Campbell* concurrences, and *Kuhajda*. **Cite it from *Unicare*.**
- ***Anderson*** / ***Allen*** — nitpicking proposals "**unnecessarily injected ambiguity into these proceedings and created more judicial labor, not less**."
- ***Pratt*** — the formalism high-water mark: "**Even where no logical apportionment can be made, it is nonetheless required.**"
- ***Lamb*** (Lewis, J.) — "purely the product of the technical language of the rule, not logic or proper legal reasoning."
- ***Suarez Trucking*** — "This is a rule of **consistency**. It is not … a rule of **regurgitation**."

## Two accountability findings

**The 21-year lag.** *Timmons*'s **Supplemental Order (Oct. 22, 1992)** records commenters lamenting that § 768.79's scope is limited to "**civil actions for damages**." The Court called that "beyond this Court's control because [it is] substantive" and asked the Rules Committee for a new rule — the origin of the 1996 rewrite. That same limitation is what *Nichols* (2006) and *Diamond Aircraft* (2013) had to resolve **by construction**. It has never been amended.

**The appellate-fees question, resolved thinly by the justice who objected.** Wells, dissenting in part in *Hannah* (1996): "[a] plain reading of the statute **does not provide for attorney fees on appeal**, and the Court should not write such a provision into the statute." **Wells then writes *Frosti* (2008)**, holding in one sentence on DCA authority that the right "applies to fees incurred on appeal" — without acknowledging his earlier position. *Coates* (2023) was therefore not writing on a blank slate. **The finding is how thinly it was answered, not that it went unanswered.**

---

# VERIFIED FACTS — do not re-derive

## Statute

Credit line, 2024 Florida Statutes: **s. 58, ch. 86-160; s. 48, ch. 90-119; s. 1175, ch. 97-102; s. 24, ch. 2022-271.**

✅ **Ch. 90-119 fully sourced** (*Timmons*; *MX Investments* quoting the 1st DCA; *Knealing* n.5; *Gulliver Academy* n.1):
- **§ 48** — rewrote § 768.79(1) and **added subsection (6)**, effective **October 1, 1990**. It let a **defendant** recover where the judgment is "**one of no liability**." Before 1990 the statute measured against "the judgment obtained **by the plaintiff**," so defendants could not recover on a defense verdict (*Rabatie*, *Kline*, *Oriental Imports*).
- **§ 22** — repealed § 45.061 as to causes of action accruing after **October 1, 1990**.

🔴 **TRAP — two different subsection (6)s. Do not conflate them.** The **(6) added in 1990** is the judgment-comparison provision (the "no liability" language and the 25% math). After **ch. 2022-271** inserted a new (6) for property-insurer conditional joint offers, **the 1990 provision became (7)**. So "§ 768.79(6)" means the judgment-comparison provision in any pre-2022 source and the property-insurer carve-out in any post-2022 source. Always tie it to a year.

✅ **§ 45.061 — full picture.** Enacted **1987** (a year *after* § 768.79, not alongside it). Repealed **prospectively** in 1990. Survives only for pre-Oct-1990 causes and remains on the books — Canady cites it as § 45.061, Fla. Stat. (2020) in *CCM*. Its **§ 45.061(2)(b)** definition of "the amount of the judgment" (costs "prior to the making of the offer") is the comparator he deploys against the *White* formula.

✅ **Ch. 2023-15 (HB 837), § 11** repealed **§ 627.428**, effective **March 24, 2023** (*Coates* n.2). It did **not** amend § 768.79.

✅ **Ch. 2022-271 renumbered § 768.79's subsections — mapping resolved from the statute August 3, 2026.** Full current numbering under THE THESIS §3. The shift: **old (6) → new (7)** (judgment comparison / 25% math), **old (7)(a)–(b) → new (8)(a)–(b)** (good faith; reasonableness factors). **(1)–(5) and (2)(b) are unchanged** — *Trace Elements* still cites § 768.79(2)(b) for "name the party making it." **Every pin cite must still be tied to a statutory year.**

⭐ **Versioning rule — *Jones Boatyard* (1993).** § 768.79 does not reach causes accruing before **July 1, 1986** (§ 768.71(2)), and the applicable version is the one in effect **when the cause of action accrued**. By contrast **§ 45.061's trigger is the making of the offer** (*A.G. Edwards*, *Leapai*). Different temporal triggers. Also **ratifies *Mudano***, closing the retroactivity loop opened in Phase 0.

✅ **Phase 1 resolved August 3, 2026 from primary documents:**
- **Ch. 87-249** created § 45.061 in section 1 and did not mention § 768.79.
- **Ch. 99-225** did not mention § 768.79; section 27 amended § 768.81.
- ⭐ **The May 24, 1990 staff analysis is retrieved.** It is a **Senate Staff Analysis and Economic Impact Statement for CS/SB 2670**. The *White* majority is correct in substance; Harding's `CS/HB 2670` is a miscitation. Page 7 states the consolidation purpose and flags the then-draft's missing § 45.061 repealer. The enrolled act cured that problem in § 22 and placed the § 768.79 rewrite in § 48.
- **Ch. 86-160 § 60** created § 768.81; the same-session-law argument is verified.

Full findings and retrieval manifest: `phase-1-findings.md` and `sources/manifest.md`. Local PDFs, when downloaded, live in the Git-ignored `sources/pdfs/` directory.

## Rule

Origin is **1972**, *In re the Florida Bar*, 265 So. 2d 21 — Florida's first offer-of-judgment rule, **identical to Fed. R. Civ. P. 68** (costs only). Confirmed by *Sarkis* and *Southeast Floating Docks*.

**1989**, *Fla. Bar re Rule 1.442*, 550 So. 2d 442 — withdrew and replaced rule 1.442 eff. Jan. 1, 1990; the new rule's **procedural aspects supersede** inconsistent statutes. ✅ **It expressly declined to reach constitutionality** — now confirmed from the opinion itself ("in this nonadversarial petition we decline to address the constitutionality of the purely substantive aspects"), as well as by *Sarkis* and *Timmons*. An earlier note here said otherwise, taken from the trial court's characterization in *TGI Friday's*.

**1996**, 682 So. 2d 105 — the rewrite to Proposals for Settlement, eff. Jan. 1, 1997. Source of **(c)(3)** and of the *Fabre* committee note. Between *Timmons* (1992) and this opinion, rule 1.442 read **in its entirety**: "Parties shall comply with the procedure set forth in section 768.79, Florida Statutes (1991)" — which is why *Hingson*, on a pre-1997 offer, had to derive apportionment from the **statute** alone.

**2013**, 112 So. 3d 1209 — out-of-cycle, unanimous; (f)(1)'s cross-reference moves from deleted rule 1.090(e) to **Fla. R. Jud. Admin. 2.514(b)**, preserving the carve-out. Reactive to another *rule*, not to a decision or statute.

**Nov. 13, 2025**, SC2025-0045 — **eff. Jan. 1, 2026**, unanimous. Mostly AOSC22-78 restyling. ⭐ **(c)(3) and (c)(4) were reopened and re-adopted with only *shall* → *must*; Committee Notes [No Change].** So the 1996 *Fabre* note is still the operative note on (c)(3) — and the Court restyled that sentence **while *Trace Elements* sat fully briefed on its own docket, four weeks before oral argument.** See Live case status for the timeline.

Full 1972 → 1996 genealogy: see the table under *Sarkis* in `sc-corpus.md`. **Full 1972 → 2025 chain with a reactivity typology: see the Phase 2 section at the end of `sc-corpus.md`.**

⭐ **Rule 1.442(g) diverges from the statute** — it runs 30 days from **entry of judgment** in a nonjury action but from **return of the verdict** in a jury action. "Since these time requirements are procedural, **the rule prevails where it differs from the statute**" (*Gulliver Academy*).

## Corpus counts (CourtListener, `fla` + `fladistctapp`)

| Query | Count |
|---|---|
| `"768.79"` | 776 |
| `"1.442"` | 514 |
| `"768.79" OR "1.442"` | 901 |
| Union, Supreme Court only | 85 |
| **Supreme Court opinions containing "768.79" at all** | **56** |

Era distribution for `"768.79"`: pre-1996 = 100 · 1996–2006 = 302 · 2006–2016 = 200 · 2016–2026 = 174. Sums to 776; independently validated by re-partitioning. **Real counts, not pagination caps.**

## Live case status

***Trace Elements, Inc. v. MacKensen*, No. SC2024-1274 (Fla. July 2, 2026)** — 4–3, Muñiz, J.; Sasso, J., dissenting with Francis and Tanenbaum, JJ.

🔴 **REHEARING IS PENDING AND UNDECIDED.** Verified against the ACIS docket printed **August 3, 2026, 8:38 a.m.** (saved at `Trace Elements/Case View - …pdf`; 48 entries; case status **Open**):

| Date | Entry |
|---|---|
| 07/02/2026 | **FSC opinion** — quashed & remanded |
| 07/10/2026 | Order — Respondents' motion for attorney's fees **denied** |
| **07/17/2026** | **Respondents' Motion for Clarification and Rehearing of July 2, 2026 Opinion** (Mackensen) |
| **07/20/2026** | **Petitioner's Response in Opposition** (Trace Elements) |
| — | **No order disposing of the motion. No mandate.** |

**The opinion is not final and the thesis is exposed until this is resolved.** Re-pull the docket before anything ships. Note the motion seeks **clarification *and* rehearing** — a clarification grant could narrow the holding without a full rehearing, which would still move the analysis.

**Procedural history worth having:**
- Trial court: **Indian River County**, Hon. **Robyn Stone**. DCA: **4th**, No. 4D2023-1707. Notice to invoke filed 08/29/2024.
- **Jurisdiction accepted 02/28/2025 — CANADY, LABARGA, COURIEL, GROSSHANS, and SASSO, JJ., concurring.** ⭐ Sasso voted to take the case and then wrote the dissent; Canady voted to take it, having spent a decade objecting to this line's jurisdictional reach.
- **Oral argument held December 11, 2025** (video available through ACIS).
- Counsel: **James W. Beagle** and Andrew A. Harris for petitioner; **Michael G. Kissner, Jr.**, Savannah J. H. Unruh, Michael Orr, and Loreyn Raab for respondents.
- Respondents sought **§ 57.105** fees against petitioner's counsel (07/25/2025); denied 07/10/2026.

⭐⭐ **The timeline finding this docket unlocks.** Jurisdiction was accepted **February 28, 2025**; briefing closed with the reply on **October 10, 2025**; oral argument was set by order of **October 27, 2025**. The Court then adopted the restyled rule 1.442(c)(3) in **SC2025-0045 on November 13, 2025 — unanimously — with this case fully briefed on its own docket and argument four weeks away.** It restyled the very sentence it was about to divide 4–3 over, and changed nothing but *shall* → *must*. Stronger than the earlier "seven months before" framing.

🆕 **New conflict case to pull:** ***Watkins v. Corbett*, No. 2D2025-0214, 2026 WL 816637 (Fla. 2d DCA Mar. 25, 2026)** — filed by petitioner on 03/27/2026 as supplemental authority "that Expressly and Directly Conflicts with the Decision on Review." Post-dates the corpus build; not yet in `sc-corpus.md`.

---

# TOOLING GOTCHAS — expensive to rediscover

## CourtListener

- **All six DCAs collapse into one court id, `fladistctapp`.** Valid Florida codes: `fla`, `fladistctapp`, `flaag`. There is no `fla1dca`/`fla4dca`.
- **The docket record does not help** — `dockets.court_id` is also `fladistctapp`, `appeal_from` is null. **This method fails; don't retry it.**
- **Four-signal district cascade** (detail in `phase-0-findings.md` §1): **S1** `download_url` hostname → `(\d)dca\.flcourts\.gov` · **S2** `docketNumber` → `^(?:Nos?\.\s*)?(\d)D(\d{2}|\d{4})-` · **S3** HTML header → `District Court of Appeal of Florida,?\s+(First|Second|…) District` · **S4** judge-panel lookup / manual.
- **Opinion text lives in one of three fields, unpredictably.** Modern → `plain_text`. Older Lawbox → `html_lawbox` (with `plain_text` empty). A third set (*Diamond Aircraft*, *Allen*, *Massey*) has **both empty** and text only in **`xml_harvard`**. Request `plain_text` + `html_lawbox` together; fall back to `xml_harvard`.
- **Big opinions exceed the tool output limit** and persist to a file. Strip markup first — `re.sub(r'<[^>]+>', ' ', …)` + `html.unescape` over `xml_harvard` cuts ~60% and makes it readable in one pass. Some persisted files have lines too long for `Read`'s offset/limit; slice by character range in Python instead.
- ⭐ **Triage before reading.** Only **56 of 85** SC opinions contain "768.79" at all — running that query alone is the cheapest filter in the project. Build a **doctrinal-density matrix** (per-arc searches + this control). It scored **~73% precision** on Tier A; it matches on **vocabulary**, so it cannot separate a holding from a quotation. The control is reliable as a **negative** filter.
- **`citeCount` is a poor relevance proxy here.** Confirmed misrankings: *Rollins* (121), *Aspen* (58), *D'Angelo* (99), *Wilson v. Salamon* (57), and likely *Manasse* (77), *Macedo* (44), *Joyce* (33). Rank by citations *within* the 768.79/1.442 set.
- **`cited_gt` does not filter** — `cited_gt: 0` returns the unfiltered count. Tier client-side.
- **The `court` parameter takes comma-separated values**, not space-separated.
- **Search fields are camelCase** (`caseName`, `dateFiled`); API fields are snake_case (`case_name`, `citations`). Don't copy one into the other.
- **Search `type=o` returns opinions, not cases.** `opinion_id` diverges from `cluster_id` for concurrences and dissents. **De-dup on `cluster_id`.** Separate dissents are usually **majority `opinion_id` + 1**; confirm via the cluster's `sub_opinions`.
- Always request `fields`.

## LegiScan

- **Florida coverage starts in 2010.** Reaches ch. 2022-271 forward; cannot see ch. 86-160, 87-249, 90-119, or 97-102.
- **Search defaults to the current session.** Scope by `year` or pull master lists per session.
- Pre-2010: Laws of Florida (laws.flrules.org), flsenate.gov year-archive (back to 1998 only), FSU law library's Florida legislative history collection.

## Retrieval trap — terminology shifted

Pre-1996 opinions say **"offer of judgment"** / **"demand for judgment."** Post-1996 they say **"proposal for settlement."** Querying `"768.79" + "proposal for settlement"` returns 320 hits with the earliest at **1997** — silently truncating a statute dating to 1986.

**Retrieve on `"768.79"` and `"1.442"` alone, union, de-dup on `cluster_id`.** Phrase terms belong in the coding layer as era markers, never in the query layer.

## Connectors needing authorization

Not usable until authorized: **Trellis** (highest value — the only route to circuit-court practice), Aurora, TopCounsel, Everlaw, Google Drive, Slack, plugin-side CourtListener. Authorize claude.ai connectors in connector settings; other servers via `claude mcp` or `/mcp` in an interactive terminal. The standalone CourtListener MCP works and is what everything above is built on.

---

# WORKING CONVENTIONS

- **Never assert a holding for an unread case.** `sc-corpus.md` tracks read status per case; keep that column honest.
- **Verify every citation with `analyze_citations`** before anything ships.
- **Convert relative dates to absolute** everywhere.
- Code each case with `district_signal` and `district_confidence` so attribution provenance stays auditable.
- Record `statute_version` and `rule_version` per case — they make the two-track timeline work by showing when a case turned on text that no longer exists.
- The formal 30-case district-attribution validation runs at the **top of Phase 3 retrieval scripting** — cheap then, expensive now.

---

# TEN DOCTRINAL ARCS

1. **Strict compliance vs. substantive purpose** — the pendulum
2. **The derogation-canon fight** — a statute canon applied to a procedural rule; rule 1.010 and *Koppel*'s threshold
3. **Joint-proposal apportionment** — § 768.79(2)(b) and rule 1.442(c)(3)
4. **Ambiguity, conditions, and nonmonetary terms** — *Nichols*; general releases; anti-nitpicking (*Anderson*, *Allen*); the 2022 reset
5. **Scope of "civil action for damages"** — *Nichols*, *Diamond Aircraft*; equitable claims; arbitration
6. **Good faith** — **§ 768.79(8)(a) post-2022; (7)(a) in pre-2022 sources**; nominal proposals (*Leapai* n.2's "one dollar offer"; *Frosti*'s $1 punitive offer)
7. **Effective date and retroactivity** — *Mudano* → *Jones Boatyard*; recurs on every amendment, including November 2025
8. **Contract formation and acceptance mechanics** — *Suarez Trucking*; the mirror-image rule; counteroffers don't terminate an offer (*Scope v. Fannelli*); ⚠️ **the "all-or-nothing, allocated offer"** — a joint apportioned proposal requiring acceptance of the whole, approved by every DCA to consider it (*Hoang Dinh Duong*, collecting cases) — **reconcile with *Gorka* and the 2022 carve-out**
9. **Calculating "judgment obtained"** — the *White* formula → *Nichols* → *Shands* → *CCM Condominium*
10. **Procedural deadlines** — rule 1.525 and rule 1.442(g); *Gulliver Academy* → *Saia* → *Frosti* → *Koppel*

---

# NEXT STEPS

**Nothing load-bearing is open.** The *Fabre* premise is verified, Phase 2 is closed, and the administrability counter has been run to ground. What remains is consolidation, drafting, and supporting research.

### The critical path

1. ✅ ~~Consolidate Phase 3 analytically~~ — **done August 3, 2026.** See `arc-matrix.md`. Three findings feed the memo: the 4–3s cluster in the apportionment arc; **arc 6 (good faith) has no squarely decided case** and is the corpus's real gap; the district work to date is the **Supreme Court's alignment matrix**, not the district-split matrix.
2. **Draft the doctrinal memo.** ⬅️ **Now the critical path.**
3. ⚠️ **Re-pull the ACIS docket immediately before anything ships.** Rehearing is pending; denial looks likely but is not certain.

### Supporting research — parallelizable, none blocking

4. **Pull the cases surfaced by the rehearing filings** (table at the end of the *Trace Elements* entry in `sc-corpus.md`): *Watkins*, *Cobb*, *Graham*, *Pacheco*, *Beal Bank*, *Ramos*/*Furen*, *Twiddy*, *C & S Chemicals*, *Herzog*. ⚠️ Also read *Hoang Dinh Duong* in full for the **all-or-nothing allocated offer** and its *Gorka* distinction — only the apportionment passage has been read.
5. 🎥 **Mine the December 11, 2025 oral argument** — `https://www.youtube.com/watch?v=HBBqn7Ya4PU`, motion cites 26:02. The Court probing administrability from the bench, four weeks after restyling (c)(3), is the best evidence it knew what it was doing.
6. **Tier B (11 cases) — light-code**, spot-checking the four high-citation entries first: *Manasse* (77), *Macedo* (44), *Joyce* (33), *Odom* (15).
7. **Tier C (9 cases)** — no mention of § 768.79; light-code. The three pre-statute rule cases (*CU Associates*, *Cheek*, *Fixel*) matter only if Phase 2 needs the 1972–1986 rule history.
8. **Verify** the five suspected false positives in `sc-corpus.md` §B and the 1980 rulemaking opinion.
9. ✅ ~~**Phase 1** — pull the 1990 staff analysis and resolve ch. 87-249, ch. 99-225, and the ch. 86-160 section number~~ — **complete August 3, 2026.** See `phase-1-findings.md` and `sources/manifest.md`.
10. **Pull the formatted SC2025-0045 slip opinion** to resolve what changed in (c)(2)(B) and (c)(2)(F) — the plain-text version loses the underline/strikethrough.
11. ✅ ~~**Confirm the ch. 86-160 section number for § 768.81**~~ — **§ 60, verified from the primary session law.**
12. Resolve the three open scoping decisions.

✅ **Closed August 3, 2026:** the *Fabre* verification · the three outstanding Phase 2 rule-amendment opinions · the *Trace Elements* rehearing status (pending) · the administrability counter-argument · the post-2022 subsection mapping · the *Gorka*-override overstatement · **all four Phase 1 legislative questions**.
