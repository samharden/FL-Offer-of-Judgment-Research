# Drafting Appendix

### Statutory language for the three scenarios

**Prepared:** August 7, 2026
**Companion to:** [`strategy-memo.md`](strategy-memo.md)

> 🔴 **Working drafts for discussion.** Not bill-ready. Subsection numbering follows the **post-ch. 2022-271** statute; every cross-reference must be re-checked against the current Florida Statutes before filing, because ch. 2022-271 renumbered § 768.79 and the trap is well documented (`CLAUDE.md`, "TWO DIFFERENT SUBSECTION (6)s").

**Convention:** **bold** = added text · ~~strikethrough~~ = deleted text · *[bracketed italics]* = drafting note.

---

## 0. The subsection map you are drafting into

Current § 768.79, post-2022:

| Subsection | Contents |
|---|---|
| (1) | Entitlement — the core right; contains the word **"penalty"** |
| (2) | Offer requirements; **(2)(b)** — "name the party making it" *(the* Hingson *hook)* |
| (3) | Service and filing |
| (4) | Acceptance |
| (5) | Withdrawal |
| (6) | **Property-insurer conditional joint offers** (new in 2022) |
| (7) | Post-judgment cost-and-fee determination — **the 25% math** |
| (8) | **Good faith** (a), and the reasonableness factors (b) |

**New material goes at (9) and (10).** Nothing in these drafts amends (3), (4), or (5) — those are service, acceptance, and withdrawal, which are rule 1.442's territory and would be superseded under *Timmons* / *Knealing*.

---

# Scenario A — The Technical Package

## A-1. Good-faith safe harbor

Amend § 768.79(8)(a):

> (8)(a) If a party is entitled to costs and fees pursuant to the provisions of this section, the court may, in its discretion, determine that an offer was not made in good faith. In such case, the court may disallow an award of costs and attorney's fees.
>
> **In an action for medical negligence governed by chapter 766, an offer is presumed to have been made in good faith if, at the time the offer was served, the offeror possessed a written medical expert opinion, as defined in s. 766.202(6), that supported the offeror's valuation of the claim, and the offer was accompanied by a written statement of the factual and legal basis for the amount offered. This presumption may be overcome only by clear and convincing evidence. The failure of an offer to be accepted, the disparity between the amount offered and the amount of any judgment, and the offeror's motive in making the offer are not, singly or in combination, sufficient to overcome the presumption.**

**Drafting notes.**

- ⭐ **The last sentence is the operative one.** Arc 6 is empty (`arc-matrix.md` finding #2), so trial courts currently deny defense fee awards on exactly these three grounds. *Anderson* already holds that **motive goes to good faith rather than validity** — this codifies that motive does not carry good faith either.
- **§ 766.202(6)** is the chapter 766 definition of "medical expert." Confirm the current subsection letter; chapter 766 has been renumbered.
- **Art. V analysis:** good faith is a creature of the statute, at (8)(a), and it defines when the substantive right to fees exists. Legislating its standard is legislating entitlement. Clean.
- ⚠️ **Consider whether "clear and convincing" is worth the fight.** A rebuttable presumption on a preponderance standard captures most of the value and draws less fire. Have it as the fallback amendment.

## A-2. Presuit fee accrual

Amend § 768.79(7) *(the judgment-comparison and award provision)*, adding at the end:

> **In an action for medical negligence governed by chapter 766, the reasonable costs and attorney's fees awarded under this section include those incurred on or after the date the notice of intent to initiate litigation was mailed under s. 766.106(2), and are not limited to those incurred after the date the offer was served.**

**Drafting notes.**

- ⭐ **This is the cleanest provision in the entire package.** *Knealing* holds that what saves § 768.79 from art. V is that it **contains a substantive fee-authorizing provision**. This provision does nothing but define the measure of that substantive award. There is no procedural component to attack.
- Value: the § 766.106 presuit period is 90 days minimum and routinely extended. Adding it to the fee-shifting window is a material increase in the cost of rejecting a proposal, obtained without touching a single procedural rule.
- ⚠️ **Retroactivity.** *Jones Boatyard* keys the applicable version of § 768.79 to **accrual of the cause of action**, not to the date of the offer. Every one of these drafts needs an effective-date clause tied to accrual, or it will not reach a single pending case and will draw a retroactivity challenge on the ones it does reach. Draft it explicitly; do not leave it to construction.

## A-3. Entitlement preservation — the apportionment fix

**Two provisions, deliberately redundant. Both are needed.**

### A-3(i) — pull the substantive predicate (the *Kuhajda* move)

Amend § 768.79(2)(b):

> (2) The offer shall:
> …
> (b) Name the party making it and the party to whom it is being made. **As used in this paragraph, and consistent with s. 1.01(1), the singular includes the plural. Nothing in this paragraph requires an offer made by or served upon two or more parties to state an amount attributable to each such party.**

### A-3(ii) — preserve entitlement directly

Create § 768.79(9):

> **(9) Entitlement to costs and attorney's fees under this section is not defeated by the failure of an offer made by or served upon two or more parties to state an amount attributable to each such party, provided the offer states the total amount and all nonmonetary terms with particularity. This subsection is a limitation on the circumstances in which the substantive right created by this section may be denied and is not a requirement as to the form or content of an offer.**

**Drafting notes.**

- 🔴 **The last sentence of (9) is doing the constitutional work and must not be cut in committee.** Rule 1.442(c)(3) is a **content** rule. A statute that regulates content collides with the rule and loses under *Timmons*. A statute that regulates **entitlement** does not collide with it at all — it simply says the rule's content requirement is not a ground for denying the statutory right. Same result, different constitutional category. *This sentence is the difference between a provision that survives and one that is superseded within a rulemaking cycle.*
- ⭐ **Why (i) and (ii) both.** (ii) works directly. (i) works *through the Court's own doctrine*: *Trace Elements* sustains (c)(3) by holding it implements the substantive requirement that *Hingson* found in the singular "party" of (2)(b). Amend (2)(b) and (c)(3) implements nothing substantive — at which point *Kuhajda* says "[t]he procedural rule should no more be allowed to trump the statute here than the tail should be allowed to wag the dog." **The Legislature never touches the rule; the Court's own precedent disarms it.**
- ⚠️ **(i) also finally answers Harding, J.** His *Hingson* dissent cited § 1.01(1) — "[t]he singular includes the plural and vice versa" — against the majority's two hedged sentences. This provision is the Legislature saying it meant what § 1.01(1) already said. **That is the framing for the bill analysis: not a change in the law, a correction of a 4–3 misreading of it, now twenty-four years old.**
- ⚠️ **Confirm the (c)(4) interaction.** Rule 1.442(c)(4) already excuses apportionment for solely vicariously liable parties. (9) swallows it. Decide whether the bill says so.

---

# Scenario B — The Asymmetric Trigger

Scenario A, plus:

Create § 768.79(10):

> **(10) MEDICAL NEGLIGENCE ACTIONS. — In an action for medical negligence governed by chapter 766:**
>
> **(a) Notwithstanding subsection (7), a defendant is entitled to recover reasonable costs and attorney's fees incurred from the date of filing of an offer of judgment if the judgment is one of no liability or the judgment obtained by the plaintiff is less than the amount of the offer.**
>
> **(b) Notwithstanding subsection (7), a plaintiff is entitled to recover reasonable costs and attorney's fees incurred from the date of filing of a demand for judgment only if the judgment obtained is at least 50 percent greater than the amount of the demand.**
>
> **(c) An award under paragraph (a) against a claimant who has obtained a judgment is enforceable only against the proceeds of that judgment and may not be enforced against any other asset of the claimant. This paragraph does not apply where the judgment is one of no liability.**
>
> **(d) This subsection does not apply to an action against a person or entity entitled to the limitations on liability in s. 768.28.**

**Drafting notes.**

- **(a) removes the 25% cushion for defendants; (b) doubles it for claimants.** These are the levers. Everything else in (10) is armor.
- ⭐ **(c) is the Article I, § 26 mitigation and it is the most important defensive provision in the package.** It removes the constitutional objection in the only fact pattern where § 26 bites — a claimant who recovers something and then owes more in fees than they recovered — while preserving the full deterrent on a defense verdict, which is the case carriers actually care about. **It also pre-empts the "this bill bankrupts widows" floor speech at near-zero cost.** Concede it early and visibly; do not let it be extracted.
- **(d) is coalition management, not constitutional law.** Public hospital districts already have § 768.28 caps and lobby on sovereign immunity rather than tort reform. Carving them out costs the commercial carriers nothing and removes a bloc that would otherwise complicate the bill. ⚠️ Confirm the interaction with the separate sovereign-immunity-limits bill moving in the same period.
- ⚠️ **Expect (b) to be the first thing cut.** Fifty percent is the most legible asymmetry in the bill. Have a fallback at 33⅓% and be prepared to trade (b) entirely for (a) — **(a) is worth several times (b)**, because the defense makes far more proposals than claimants make demands.
- 🔴 **Findings section is mandatory.** See `strategy-memo.md` § 6.3. Cite OIR closed-claim data under § 627.912, and quote *Gorka* ("in sharp contrast to the intended outcome") and the *Allen v. Nunez* dissent ("inconsistently applied and unpredictable"). A findings section resting on the Court's own characterizations is materially harder to attack under *McCall* than one resting on premium data.

## Optional B-2 — the construction directive

Consider, and weigh carefully:

> **(11) This section shall be construed liberally to effectuate its purpose of encouraging the settlement of medical negligence actions. The characterization of an award under this section as a penalty in subsection (1) does not require that this section, or any rule implementing it, be strictly construed.**

⚠️ **Recommendation: do not file this in the first bill.**

- **What it targets:** § 768.79(1)'s word "penalty" is the premise for strict construction in *Sarkis* and for *Coates*'s holding that this is not a prevailing-party statute. *Willis Shaw* then extended the derogation canon **from the statute to the rule**. Neutralizing "penalty" would blunt the canon at its root.
- **Why not yet:** (i) *Coates* and *Koppel* together say that **where the text is clear, no canon applies at all** — the modern Court's declared method may already be doing this work without a statute; (ii) telling the Court how to construe **"any rule implementing it"** is a direct instruction about the Court's own rules and is the most art.-V-provocative sentence anyone could put in this bill; (iii) it invites the Court to reach the construction question in a posture the carriers do not choose.
- **Hold it in reserve** for a second bill, after the first has been construed.

---

# Scenario C — The *Echarte* Play

**Structure:** a new § 766.2085, plus one conforming sentence in § 768.79. Do **not** rebuild § 768.79's machinery.

## C-1. The conforming amendment

Create § 768.79(12):

> **(12) This section does not apply to an offer made under s. 766.2085. A party may not serve an offer under this section and an offer under s. 766.2085 as to the same claim.**

## C-2. The mechanism

Create § 766.2085, **Qualified offer of resolution**:

> **(1) LEGISLATIVE INTENT. — It is the intent of the Legislature to provide claimants and defendants in medical negligence actions a voluntary mechanism for prompt, certain resolution, and to provide a claimant who accepts such an offer a benefit commensurate with any limitation on damages that results from declining it. This section is modeled on the voluntary binding arbitration process established in ss. 766.207 and 766.209.**
>
> **(2) THE OFFER. — A defendant may serve a qualified offer of resolution, which must be accompanied by:**
> **(a) A written medical expert opinion, as defined in s. 766.202(6), supporting the offeror's valuation of the claim;**
> **(b) A stipulation to the entry of judgment against the offeror in the amount offered; and**
> **(c) An irrevocable commitment to pay the amount offered within 30 days after acceptance.**
>
> **(3) ACCEPTANCE. — Upon acceptance, judgment shall be entered in the amount offered, the amount shall be paid within 30 days, and the claimant shall additionally recover reasonable attorney's fees not to exceed 25 percent of the amount of the award, together with taxable costs.**
>
> **(4) REJECTION. — If a claimant rejects a qualified offer of resolution and the judgment ultimately obtained does not exceed the amount of the offer:**
> **(a) The claimant's recovery of noneconomic damages is limited to $______ per claimant, adjusted annually for inflation; and**
> **(b) The defendant is entitled to reasonable costs and attorney's fees incurred from the date the offer was served, enforceable as provided in s. 768.79(10)(c).**
>
> **(5) NO OFFER. — If no qualified offer of resolution is served, this section imposes no limitation on the damages recoverable by a claimant.**
>
> **(6) This section does not limit any party's right to trial by jury.**

**Drafting notes.**

- ⭐ **(3) is the *Kluger* "commensurate benefit" and it must be generous.** ⚠️ It deliberately mirrors § 766.209(3) — the provision under which a claimant recovers damages plus **fees up to 25 percent of the award** where the defendant refuses arbitration. That is the benefit *Echarte* found sufficient. **Do not let (3) be trimmed to save money; it is the constitutional consideration, not a cost line.**
- ⭐ **(5) and (6) exist to defeat the access-to-courts framing.** Nothing changes for a claimant unless a defendant chooses to make an offer *and* the claimant chooses to reject it. **Every consequence in this section is downstream of two voluntary choices** — which is materially better than § 766.209(4), whose consequence attaches to a claimant who refuses arbitration regardless of the merits.
- 🔴 **The figure in (4)(a) is the whole fight.** Set it at or above the § 766.209(4) benchmark ($350,000 per incident) and index it. A lower number reads as § 766.118 revived under a new name and invites the Court to treat it as one; ⚠️ the § 766.118 caps were struck in *McCall* and *Kalitan*, and a number that looks like them is the surest way to draw that comparison. **The "this is the arbitration scheme's sibling" argument only works if the number is a sibling too.**
- ⭐ **(1)'s last sentence is written for the opinion, not for the practitioner.** Legislative intent that names *Echarte*'s statutes and adopts their structure gives the Court a ready-made path to upholding this without writing anything new. Make the path short.
- 🔴 **Before any of this is filed, read *Echarte*, *McCall*, *Kalitan*, *Franks v. Bowers*, and *Kluger* in full, and resolve whether *McCall*/*Kalitan* undermine *Echarte*'s reasoning.** That question is unresearched (`strategy-memo.md` Part 8) and it determines whether Scenario C is a 60–70% proposition or a much worse one.

---

# Cross-cutting drafting checklist

| ✅ | Item | Why |
|---|---|---|
| ☐ | **Effective date tied to accrual of the cause of action** | *Jones Boatyard*. Without it the amendment reaches nothing pending and draws a retroactivity challenge on what it does reach |
| ☐ | **No provision regulating the timing, form, service, or content of an offer** | *Knealing* struck § 44.102(6) for exactly that |
| ☐ | **Every provision framed as entitlement, measure, or damages consequence** | The three substantive categories that survive art. V |
| ☐ | **Classify by action ("an action for medical negligence governed by ch. 766"), never by party or by insurer** | Art. III, § 11; and it keeps the classification conduct-based, which is *McCall*'s distinction |
| ☐ | **Contemporaneous findings, 2026–2027 data, § 627.912 closed claims** | *McCall*'s stale-findings holding |
| ☐ | **Findings quote *Gorka* and the *Allen* dissent** | Rational-basis armor written by the Court itself |
| ☐ | **Art. I, § 26 non-recourse mitigation present in every scenario** | The one objection unique to medical malpractice |
| ☐ | **Severability clause, provision by provision** | A-1 and A-2 must survive if A-3 or (10) falls |
| ☐ | **Every subsection cross-reference re-verified against the current statute** | Post-2022 renumbering; two different subsection (6)s |
| ☐ | **Companion comment filed with the Civil Procedure Rules Committee** | The Court can undo any procedural component in one rulemaking cycle |

---

*Companion: [`strategy-memo.md`](strategy-memo.md). Sources: [`README.md`](README.md).*
