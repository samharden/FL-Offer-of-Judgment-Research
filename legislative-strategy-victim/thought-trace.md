# Thought Trace

### How this folder was approached

**Written:** August 7, 2026, immediately after producing [`strategy-memo.md`](strategy-memo.md), [`draft-language.md`](draft-language.md), and [`README.md`](README.md).

> This is a record of **method and reasoning**, not of findings. It exists so the analysis can be audited: which conclusions came from primary sources, which came from structural inference, which came from a guess that survived a check, and where the reasoning is load-bearing enough that being wrong would collapse a scenario.
>
> It is written after the fact but not reconstructed sympathetically — the wrong turns are in here because they are the useful part.

---

## 1. Orientation, and the discovery that reframed the task

**The ask:** a new folder, a strategy to tip § 768.79 toward victims of intentional torts, two or three plausible scenarios, the moves each requires, odds of passage and of surviving the Florida Supreme Court.

**First move:** read the parent project before anything else — [`../memo.md`](../memo.md) for the regime, [`../phase-1-findings.md`](../phase-1-findings.md) for how the project treats legislative history. `CLAUDE.md` was already in context and carried the doctrinal spine.

**Then a `ls` turned up something that changed the shape of the job:** [`../legislative-strategy-insurer/`](../legislative-strategy-insurer/) already existed, untracked, dated the same day — **the identical exercise run from the medical malpractice carrier's chair.**

That mattered three ways, and I decided all three before writing a word:

| Consequence | Decision |
|---|---|
| There is a house style for this genre in this project | Read the carrier memo **in full** and match its structure, its odds format, its ⭐/⚠️/🔴 convention, and above all its two disciplines: a "case against" part and an "unverified" part |
| The two folders are mirror images and will be read together | Cross-reference explicitly, and **name the places where the two sides converge** — those are the most interesting findings in either document |
| A mirror can be lazy | 🔴 **Do not simply invert the carrier memo.** The victim side has a genuinely different constitutional profile. If the structure came out identical, that would be evidence I had stopped thinking |

The third point is the one I had to keep enforcing. The A/B/C shape (small technical ask · large structural ask · big constitutional-pedigree play) survived because it is a good shape for this kind of paper, not because it was already there. But the **gates** deliberately came out different — four instead of three — and that difference turned out to be the memo's best structural finding.

---

## 2. The analytical problem I nearly got wrong

**The trap, stated plainly: § 768.79 is symmetric on its face.** A claimant who serves a demand and beats it by 25% recovers fees exactly as a defendant does. My first framing assumed asymmetry and started designing remedies for it. That framing would have produced a memo that begged its own question, and a competent opponent would have opened with it.

So I stopped and made myself answer: **why does a facially symmetric statute land unevenly on this class of claimant?** Four structural answers, and only one of them is obvious:

1. **Bimodal damages.** The 25% differential exists to absorb ordinary valuation error. Intentional-tort recoveries are credibility-dependent and noneconomic-dominated — the distribution is not merely wide, it is two-humped. A claimant answering a proposal in a case that will produce $2 million or zero is not making a valuation judgment. **The statute contains no mechanism that notices the difference.**

2. ⭐ **The § 768.72 point — the best thing in the memo, and it came from a specific question.** I asked: *what does Florida law forbid the claimant to do at the moment the claimant must answer the proposal?* The answer was sitting in chapter 768. § 768.72(1) bars pleading punitive damages without a judicial finding of a reasonable evidentiary basis; rule 1.442(c)(2)(E) lets the defense price the punitive claim at a nominal figure; *Frosti* shows a $1 proposal going unchallenged. **A proposal served before the § 768.72 ruling asks the claimant to value a claim the claimant is not yet permitted to assert.** That is not a fairness argument — it is an argument that the statute's arithmetic is being run on a forbidden number, which is a much better thing to put in front of a committee.

3. **The proposals come from the party that is not the wrongdoer.** Intentional acts are ordinarily excluded from liability coverage, so the perpetrator is uninsured and often judgment-proof and serves no proposals. The proposals come from the institutional co-defendant sued in negligent hiring, retention, supervision, or security. **This produced the single most important drafting constraint in the folder** — a carve-out written around the *claim pleaded* reaches only the perpetrator, against whom the exposure was never the practical problem. Everything in draft B-1(b) exists because of this.

4. **The empty good-faith arc**, already documented at [`../arc-matrix.md`](../arc-matrix.md) finding #2.

⚠️ **Note honestly what these four are: structural inference, not counted outcomes.** None of them rests on data about how § 768.79 actually resolves in intentional-tort cases, because that data does not exist in this project. Part 10 of the memo says so and Part 9.1 turns on it.

---

## 3. What I chose to verify, and why those things

The parent project's convention is "never assert a holding for an unread case," and the carrier memo's weakest feature is that six load-bearing cases in it are unread. I wanted this folder to have **less** of that, so I spent the verification budget on **primary statutory and constitutional text**, which is cheap to pull and dispositive, rather than on case law that would have to be read in full to be usable.

Targets, in the order I picked them and the reasoning:

| Target | Why I went after it | Outcome |
|---|---|---|
| **§ 768.79(1)** scope clause | Scenario B's whole premise is that the Legislature owns this clause. Needed the exact words | ✅ "any civil action for damages filed in the courts of this state" |
| **§ 768.72(1), (2)(a), (3)** | The § 768.72 insight needed the actual proffer standard and an actual statutory definition of intentional misconduct | ✅ Both, plus the (3) corporate standard — which is what makes draft B-1(b) reach the institution |
| ⭐ **§ 768.735** | Hunch: chapter 768 might already treat abuse cases differently. **This was the highest-yield guess in the project** | ✅ Verbatim: the Legislature has *already* exempted child abuse, elder abuse, and abuse of the developmentally disabled from three of part II's damages provisions. Scenario B stopped being a novel classification and became an argument from consistency |
| **§ 772.11** | Looking for an enacted Florida template for an asymmetric fee standard | ✅ Better than expected — claimant recovers on prevailing, defendant only on "a finding that the claimant raised a claim that was without substantial fact or legal support." Also supplied the presuit-demand model for C-2 |
| **Art. I, § 16(b)** | The carrier memo's best move is that art. I, § 26 is a constitutional provision existing *only* in med-mal. I went looking for the victim-side equivalent | ✅ "full and timely restitution in every case and from each convicted offender," self-executing. Became Scenario C's anchor |
| **§ 95.11** | Needed the long-tail provisions for the retroactivity analysis | ✅ — and corrected me, see §4 |
| **§ 787.061** | Wanted a one-way, victim-only fee statute | ✅ but much narrower than I assumed, see §4 |
| **LegiScan, FL, "768.79"** | Has anyone tried this? | ✅ No 2026 bill touched § 768.79. Useful negative |
| **FJA lobbyist registration** | The carrier memo has a coalition table built from this source; symmetry required one | ✅ 8 lobbyists, already on HB 1269 and HB 6003 |

**What I deliberately did not do:**

- **Did not read *Kluger* or *McCall*.** They are cited in the sibling folder as unread. Rather than inherit that debt, I **redesigned around it** — Gate 2 is open regardless of what *Kluger* says, and *McCall* is used only for a drafting caution ("classify by conduct, not identity"), not for a holding. **A proposition that would collapse if the unread case says something unexpected does not belong in a memo.** That is the rule I applied.
- **Did not build the DCA corpus.** ~816 opinions, flagged as untouched in the parent project. It is the right answer to the empirical question and it is a separate project. I said so rather than papering over it.
- **Did not spawn subagents.** The task was research plus judgment plus drafting, all of which needed the parent corpus in context. A cold agent would have re-derived what was already loaded.

---

## 4. Three corrections that changed the text

Recorded because each one would have put a false statement in a document written to be filed.

**(a) § 787.06(13) → § 787.061.** I assumed the human-trafficking civil cause of action lived at § 787.06(13). It does not — that subsection is about contractor affidavits. § 787.061 is the civil action, and it is **narrower than I wanted**: it runs against adult theaters specifically. I kept it, because it still does the job I needed (an enacted Florida statute giving fees to a victim with no prevailing-defendant provision at all), but the memo describes it accurately rather than as a general trafficking remedy.

**(b) § 95.11(9) → §§ 95.11(8) and (10).** I had the wrong subsection numbers for the abuse and sexual-battery limitations provisions. Pulling the statute fixed it — and (10) turned out to be stronger than what I had been reaching for: **no limitations period at all** for a § 794.011 claim where the victim was under 16. That fact is what makes Gate 4 bite.

**(c) 🔴 The Rhode Island conflation.** A search result asserted a Florida revival window for institutional childhood-sexual-abuse claims, July 1, 2026 – June 30, 2028. If true it would have been a major political fact — an organized survivor constituency that had just won, and a wave of new claims about to meet § 768.79. **It is Rhode Island.** A second search caught it. I recorded the near-miss in the memo's unverified table rather than silently dropping it, because the next person to search this will hit the same result.

⚠️ **The general lesson, and it is the one worth carrying:** the marketing-site tier of legal content mixes jurisdictions freely. Anything from that tier is a lead, never a fact.

---

## 5. How the scenarios were chosen

I did not start from three scenarios and fill them in. I started from a **lever inventory** — what are the actual mutable parts of this statute? — and then asked which combinations were coherent asks.

Six levers emerged: scope · directionality · good faith · the comparator · recourse · the defendant's own exposure. The scenarios are the natural groupings.

**Scenario A (technical)** collects the levers that operate on the *proposal* rather than the claim. That grouping is not arbitrary — it is exactly the set that escapes the retroactivity problem, which is why the memo says A and B are complements rather than alternatives.

**Scenario B (scope)** is the one the user's question is really about, and it is where I spent the most thought. Two decisions:

- 🔴 **B-1 (full exclusion, neither side recovers) over B-2 (one-way).** My instinct was B-2 — it is more valuable to claimants. I talked myself out of it on three grounds, and the third decided it: (i) B-1 is honestly neutral, which is the entire political case; (ii) B-1 *reduces* litigation, which fits the frame the Legislature actually uses; (iii) **a claimant's fee entitlement against an uninsured, judgment-proof perpetrator is worth approximately nothing**, so B-1 gives up less than it appears to. Recommending against my own first instinct is recorded here because the memo presents B-1 as the recommendation and the reader should see that it was contested.
- ⭐ **The pleading-manipulation objection, and how the answer was found.** I identified early that the thing most likely to kill B is: *any plaintiff can claim the exemption by adding a battery count.* That is a fair objection. Keying the carve-out to a **verdict** solves it but creates a chicken-and-egg problem — the parties must know at the time of the proposal whether the statute applies. I was stuck between two bad options until I noticed that § 768.72 **already supplies a mid-case judicial finding on an evidentiary record**, with its own body of law and its own certiorari review. **The screening device the carve-out needed already existed in Florida practice.** That is the single best drafting move in the folder, and it came from re-reading a statute I had already pulled for a different reason.

**Scenario C (convicted offender)** started as the weakest of the three and got promoted. Initially I had it as the small ask that passes — true but boring. The reframing came from asking *what is C worth if it passes and nothing else does?* Answer: not much on its own, because it misses the institutional defendant. **But it creates a statutory category — "an action arising from conduct for which the defendant was convicted" — that Scenario B later widens.** Legislatures widen categories they have already adopted far more readily than they adopt new ones. That turned C from the consolation prize into the recommended first filing, and it drove the whole sequencing recommendation in Part 7.1.

⚠️ **Flag on that reasoning:** the "categories get widened" claim is a generalization about legislative behavior, not a finding about Florida. It is plausible and it is unsourced. It is doing real work in the recommendation and it should be tested before anyone acts on it.

---

## 6. The gates, and where the memo's best structural finding came from

I took the carrier memo's three gates as a starting point and then asked, gate by gate, whether it actually applies on this side. That is where the memo stopped being a mirror.

| Gate | What happened |
|---|---|
| **Art. V** | ⭐ **Stronger here, and I could prove why.** *Knealing* says § 768.79 survives *because* it substantively authorizes fees — so the Legislature owns that authorization and can withdraw it. Then I remembered the *Timmons* Supplemental Order from the parent project: the Court said this exact clause is "beyond this Court's control because [it is] substantive" and referred it out. **Thirty-four years, two constructions, zero amendments.** That is not an inference; it is the Court handing the Legislature the pen and the Legislature not picking it up |
| ***Kluger* / access to courts** | **Collapsed on inspection.** It is the carrier memo's central obstacle, and it simply does not engage here — removing a fee exposure enlarges access. I nearly kept it as a gate out of structural symmetry. **Deleting it was the right call and it is why the constitutional odds run high across the board** |
| **Equal protection** | Survived, but the useful work was finding § 768.735(1) so the classification stops being novel |
| 🔴 **Retroactivity — new** | **The best find in the gates section, and it arrived by accident.** I pulled § 95.11 for background colour. Reading it next to *Jones Boatyard* (version keyed to *accrual*, via § 768.71(2)) produced the collision: **the claimants with the most § 768.79 exposure are the ones a 2027 amendment would reach last**, and a § 95.11(10) claimant filing in 2028 on 1990s conduct would be governed by the 1997 statute. The carrier memo does not need this gate because med-mal claims have short tails. **This is the clearest case in either folder of a finding that exists only because the two documents were written from different chairs** |

⭐ **And filling in the odds table produced the memo's high-level claim, which I did not anticipate.** Every constitutional number came out high and every political number came out low — the exact inverse of the carrier folder. **On this side of the statute, surviving the Court is the easy part.** That has a practical consequence I put in the memo: the effort belongs in committee and coalition work, not in constitutional briefing.

---

## 7. Honesty discipline — the specific things I refused to write

The parent project's conventions made most of these automatic. Recording them so the restraint is auditable.

- **Did not claim art. I, § 16(b) reaches civil fee awards.** The natural reading is that it addresses criminal restitution under § 775.089. I found no authority either way. So the memo does two things: says plainly that it appears to be a question of first impression, **and then explains why Scenario C does not need it to win** — § 16(b) is a *rationale* under rational-basis review, not a gate the bill must clear. Locating the weakness and then routing around it is better than either overclaiming or dropping the argument.
- **Did not assert holdings for *Kluger* or *McCall*.** See §3.
- **Did not claim intentional-tort claimants fare badly under § 768.79 as an empirical matter.** I have no counts. Part 1 is labelled as reasoning from structure, and Part 10 says the data does not exist.
- **Did not soften Part 9.1.** The strongest objection is that § 768.79 is a sword too and B-1 breaks it. The memo says that if the missing data cuts the other way, **Scenario B is affirmatively bad for claimants and should be dropped.** A strategy paper that cannot name the condition under which its centrepiece is wrong is not worth much.
- **Did not smooth over draft B-1's rough edge.** The interaction between a claim-by-claim carve-out and *Frosti*'s whole-net-judgment rule is not fully worked out. It is flagged in the drafting notes as the most likely defect in the appendix rather than left for someone to find.
- **Marked the odds as judgments.** They are calibrated against observable facts — HB 1269 died in subcommittee without a hearing; the § 627.428 repeal is three years old; C has no natural opposition — but they are estimates and the memo does not dress them as anything else.

---

## 8. What I would do next, in order

1. 🔴 **Research the proposal-date applicability clause against *Jones Boatyard* and § 768.71(2).** Gate 4 and draft B-1(d) both rest on it and it is unresearched. **Highest-value open question in the folder.**
2. 🔴 **Search for any application of art. I, § 16(b) outside criminal restitution.** Cheap; changes how hard Scenario C's findings section can push.
3. 🔴 **Build the DCA corpus.** It resolves Part 9.1, and until it is built the recommendation to run Scenario B is provisional. It is also the parent project's own most valuable extension — the same work serves both.
4. **Re-pull the *Trace Elements* docket.** Rehearing was pending as of August 3. Part 7.2's rulemaking-flank recommendation depends on it.
5. **Work the *Frosti* interaction in draft B-1.**
6. **Test C-1(b)'s retained-jurisdiction clause against rule 1.525 and *Saia*.** Noted in the memo with the irony intact: it is the one provision in a package designed to be unamendable by the Court that may need the Court's cooperation.

---

*Deliverables: [`strategy-memo.md`](strategy-memo.md) · [`draft-language.md`](draft-language.md) · [`README.md`](README.md). Mirror-image analysis: [`../legislative-strategy-insurer/`](../legislative-strategy-insurer/).*
