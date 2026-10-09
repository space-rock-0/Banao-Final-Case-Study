# Submission Form: Client B, Structural Steel

Full reasoning and arithmetic sit in `case-study.md`. Currency is INR. Items marked **(A)** are assumptions, listed in Appendix A of the case study with the question and the week that replaces each one.

## 1) In two sentences: what is the client's real problem, and how is it different from what they asked for?

The client cannot see where its steel, its trailer hours and its revision losses go, so nobody can tell which of six ideas pays, and the data to find out already sits in Strumis, CarTrack and the booking system. They asked for AI to optimise nesting; what they need is a measured loss baseline obtainable in four weeks from past nests, a first build that covers all three sources of material loss, and a delivery partner who shows a result this month.

## 2) Who are the people in this deal, and what does each of them need to hear from you?

| Person | Wants | Needs to hear from me |
|---|---|---|
| Cost Control engineer (contact, reports to his office this week) | A plan he can forward and defend | A ranked plan with a week-2 result, one fixed price, and a stop gate at week 4 |
| Management | Fewer hired trailers, lower steel cost | Rupee ranges with assumptions stated, and that they can stop at week 4 for INR 22 lakh |
| Nesting team (never on a call) | To keep a method they believe beats software | They approve every nest, they own the rules, and we test their claim fairly with them present |
| Engineering (drawings) | Not to be blamed for revisions | The register labels causes with their confirmation. Its purpose is claim-back, not blame |
| Purchasing, store yard | Material on time, easier retrieval | Location logging starts week 3; yard and purchase sizing follow once the data exists |
| Transport and dispatch | Equipment when needed | The week-2 report shows idle capacity and they confirm the avoidable list |
| Planning, estimation, IT | Reliable dates, prices, a stable Strumis migration | Later phases feed them data; the tool reads exports so the migration cannot break it |
| The team that owns cost loading (not yet identified) | Project cost integrity | One question: may a purchased plate move between projects at book cost? |

**The uncomfortable part.** Four of the six groups who decide whether this engagement survives have never had a conversation with us. Our entire evidence base is one engineer who says he sees nesting "from the outside."

## 3) The five questions you would ask on the next call, ranked. For each one: why it matters, and what you assumed while you wait for the answer.

| # | Question | Why it matters | Assumed meanwhile |
|---|---|---|---|
| 1 | Can I export read-only from Strumis (nests, parts, stock, remnants, purchases, revisions)? | Decides whether the replay can start in week 3. Everything downstream depends on it | Nests, stock and purchases export. Revisions are partial |
| 2 | Which rules do nesters follow that automatic nesting ignores (direction, bevels, common cuts, cut order, minimum usable offcut)? | Explains "hand beats auto" and defines the constraint checker that makes the comparison fair | They shape remnants for reuse and respect machine limits that default settings ignore |
| 3 | What was tonnage by product and thickness over 12 months, and does 80,000 t mean purchased steel? | Sets plate share, which material carries the loss, and the size of the prize | Purchased steel, plate 15% **(A)** |
| 4 | Can one purchased plate be shared between two projects at book value, and who owns that decision? | Decides whether the largest value pool is a build item or only a report | Unresolved. His words: "I'd have to check with my team." We build nothing that depends on the answer |
| 5 | How many trailer-days do you hire per month, at what rate, and who approves a hire? | Sizes the fleet saving, and the week-2 result proves it | 90 trailer-days a month at INR 6,000, 40% avoidable **(A)** |

Note on question 4, because the notes are easy to misread. Two different things get conflated. **Reusing an offcut on a later project already happens** — the client said "When they nest new projects, they check the offcuts first to see if anything can be used." **Sharing one purchased plate between two projects is unresolved** — cost loads to the project that bought it, and the contact was unsure and went to check. Treating the first as blocked would have thrown away the largest pool in the case; treating the second as settled would have built against an accounting policy we do not own.

Three further questions are in section 2 of the case study: revision frequency and cause tagging, approvers and budget holder, and which projects are live rather than on hold.

## 4) Which options did you consider, and why did you pick the one you did? What did you rule out, and why?

| Option | Verdict | Reason |
|---|---|---|
| A. Build a new AI nesting engine | Ruled out | Strumis has the geometry engine. A new one costs most and has no baseline to improve on |
| B. Buy or tune packages | Ruled out | The other supplier offers this. The client wants a team that develops and delivers, and nobody would own the integration |
| C. Measure and report only | Ruled out | Management gets a document with no decision attached. That is billing for an answer they already suspected |
| D. Replay benchmark, then a remnant-aware Yield Advisor on Strumis, human approved | **Picked** | Largest pool (INR 1.2 to 2.4 crore a year), data exists, answer by week 4, works inside the per-project cost rule, and builds the remnant register that later phases need |
| E. Start with the fleet | Quick win only | Real pain, but about INR 26 lakh a year beside nesting |

Alongside D we run a week-2 fleet report and a drawing revision register, because both use data the client already holds and the register supports claim-back.

**Ruled out of this engagement:** a new nesting geometry engine, cross-project plate sharing (the cost-loading answer is outstanding, so we report missed reuse in rupees instead), a yard system and a trailer load planner (both need data first), auto-release of nests without a named approver, and gain-share pricing (it needs a verified baseline, so it is offered for phase 3 with a cap).

## 5) How will the client know the pilot worked?

| Element | Answer |
|---|---|
| Metric | Net material loss %, plate and profile separately, weighted to overall. Net loss = purchased mass minus part mass minus usable remnant mass |
| Baseline | Hand nests from 6 months of closed projects: at least 40 nests, 5 projects, stratified by thickness and section, read from Strumis records |
| Threshold | Advisor beats hand nests by at least 0.5 percentage points overall, lower bound of the 90% interval above zero, zero rule violations, at least 80% rated buildable. Target 1.0 point |
| Runs | Replay: 40 nests, three arms (hand, Strumis automatic default, Strumis automatic tuned, Advisor). Pilot: two live projects, 4 weeks shadow then 6 weeks assisted |
| Who measures | Our data engineer from Strumis records, checked by the nesting approver and co-signed by Cost Control. Nesting team does the blind review of 15 pairs. Cost Control weighs scrap from 10 plates a week as an independent check on the ledger |
| Stop | Replay below 0.25 points, or constructability failures I cannot fix in two weeks. Pilot: after six assisted weeks, gain below 0.3 points, or nester acceptance below 50% |
| Why this test is feasible | The replay cuts no steel and needs no live project, so it runs while projects are on hold. Only the six-week pilot needs live projects, and it runs on whichever two exist |

**The threshold in the client's money.** One tenth of a percentage point of overall loss is 80 t, which at INR 30,000 net a tonne is INR 24 lakh a year. Half a point is 400 t and INR 1.2 crore, more than twice our fixed price of INR 55 lakh. So the gate is set where the prize clears the cost by a wide margin.

**Why not a live A/B trial.** Cutting both arms on live projects doubles steel consumption on those nests and needs live projects the client may not have. The replay avoids both problems and still produces paired, comparable arms.

## 6) What does this cost the client, and what does it cost us to deliver? Show the arithmetic and name the pricing structure. What value does the client get, in their money?

**Our cost.** 128 person-days across four roles at assumed fully loaded daily costs **(A)** of INR 30,000 (FDE lead), 24,000 (ML and optimisation engineer), 18,000 (data engineer) and 12,000 (analyst).

| Phase | Person-days | INR |
|---|---|---|
| 0, weeks 1 to 2 | 20 | 4.20 lakh |
| 1, weeks 3 to 8 | 60 | 12.96 lakh |
| 2, weeks 9 to 16 | 48 | 10.56 lakh |
| Labour | 128 | 27.72 lakh |

Hosting INR 1.20 lakh for 16 weeks plus 15% contingency on labour at INR 4.16 lakh gives **INR 33.08 lakh total cost**.

**Price and payment structure.** Fixed price **INR 55 lakh for 16 weeks**, a 39.9% gross margin, paid 20% at kickoff, 20% at the week-4 gate, 30% at week 8 and 30% at week 16. The client can stop at week 4 and owes INR 22 lakh. After week 16: INR 1.5 lakh a month support, INR 0.4 lakh hosting, language model usage passed through at cost (about INR 0.03 lakh a month for 500 revisions at about INR 5 each). Phase 3 can be quoted as a fixed module price or as 10% of verified net saving above the ledger baseline, capped at INR 60 lakh a year.

Billing front-loads on purpose: weeks 1 to 8 carry the delivery risk, so 40% falls due by week 4. If the gate says stop, we have spent roughly half of phases 0 and 1 against INR 22 lakh received and absorb the rest.

**Value to the client.** Assumptions **(A)**: steel INR 60,000 a tonne, scrap INR 30,000, net loss INR 30,000 a tonne; 90 hired trailer-days a month at INR 6,000 with 40% avoidable; revision-related scrap 0.4% of tonnage with 25% recoverable.

| Scenario | Arithmetic | INR a year |
|---|---|---|
| Conservative, nesting | 0.5 pts x 80,000 t = 400 t x 30,000 | 1.2 crore |
| Conservative, fleet | 90 x 12 x 6,000 = 64.8 lakh, x 40% | 26 lakh |
| **Conservative total** | | **1.46 crore** |
| Base, nesting | 0.75 pts = 600 t x 30,000 | 1.8 crore |
| Base, fleet + claim-back | 26 lakh + (0.004 x 80,000 = 320 t x 60,000 x 25%) | 74 lakh |
| **Base total** | | **2.54 crore** |
| Target, nesting | 1.0 pt = 800 t x 30,000 | 2.4 crore |
| **Target total** | | **3.14 crore** |

Claim-back is the least certain line. Payback on the conservative case is 55 / (146 / 12) = **4.5 months** of full operation; the base case repays in under three. Break-even against the fixed price is 183 t a year, about 3.5 t a week. At INR 20,000 or INR 40,000 net a tonne, the conservative nesting value moves to INR 80 lakh or INR 1.6 crore. Savings appear one purchase cycle after roll-out because steel is bought before the nest exists. All rupee inputs are placeholders until the client's ledger replaces them in week 1.

## 7) Timeline. What is the first result the client sees, and when? Which steps depend on the client rather than on us?

**First result: week 2**, the trailer and equipment utilisation report from CarTrack and booking data. It needs no build, no Strumis access and no client decision, and it answers the complaint management is currently unhappy about.

| Week | Result | Depends on the client |
|---|---|---|
| 2 | Fleet report and loss baseline v0 | Booking and CarTrack export |
| 4 | Gate 1: replay result, go, tune or stop | Nesting team review time |
| 8 | Advisor v1 and revision register in staging | Nesting rules, revision access |
| 14 | Pilot measured on two live projects | Two live projects chosen (week 8) |
| 16 | Gate 2: roll out, extend or stop | Management decision |

**Client dependencies.** D1 read-only exports (week 1). D2 a named nest approver and two nesters at about four hours a week (week 1). D3 the cost-loading answer (week 2). D4 12-month tonnage by product and thickness (week 1). D5 two live projects for the pilot (week 8).

The week-2 fleet report needs no Strumis access, so a late D1 delays gate 1 by the same number of weeks and leaves the first result intact. Each week D1 slips moves gate 1 by a week.

## 8) Where did you push back on the client, narrow their ask, or tell them not to do something?

| # | Pushback | What it cost me |
|---|---|---|
| 1 | Told them not to wait for a long live trial. A replay on past nests gives the answer in four weeks and cuts no steel | The more impressive-sounding demo |
| 2 | Widened their ask: "nesting" became material yield, because layout, stock length and leftovers are three sources of waste and a layout tool fixes one | A narrower, easier-to-sell scope |
| 3 | Narrowed six areas to three projects now and four later, with a data trigger for each deferral | Four workstreams of scope |
| 4 | Refused to build cross-project plate sharing, the largest pool in the case | The biggest number in any business case I could have written |
| 5 | Refused to build a new nesting engine, since Strumis has one | The build they named as their first pick |
| 6 | Told them the nesting team's claim that "auto wastes more" is a hypothesis, and I will test it with their team present and tuned settings | The easy path of taking their word for it |
| 7 | Put a stop gate at week 4 into my own price, capping their downside at INR 22 lakh | 40% of my revenue |
| 8 | Declined gain-share until a verified baseline exists | The structure a client usually wants to hear |
| 9 | Told them never to let a nest reach the factory without a named approver | My ability to run unattended |
| 10 | Flagged that 80,000 t a year and 7,000 to 8,000 t a month disagree, and chose 80,000 t | Nothing, but it needed saying |
| 11 | Told them the revision register is for claim-back and cause tracking, and every label needs an engineer's confirmation | Automation of a step they might have wanted silent |

Pushback 4 is the one I expect to be resented, and it is the one I would defend hardest.

## 9) What is most likely to go wrong with your plan, and what in these notes did you not trust?

**Most likely to go wrong.**

1. **The nesting team rejects the Advisor.** High chance, high impact. They approve every nest and own the rules. I mitigate with their approval on every proposal, a blind review, and their rules inside the checker.
2. **The Strumis export is thinner than assumed.** Question 1 settles it in week 1. I fall back to nest reports and manual extracts for the replay set.
3. **The replay misses conditions the nesters faced** (stock on that date, deadlines). I rebuild stock by date and compare only plate-internal yield where I cannot.
4. **Projects on hold leave too few live nests.** The replay carries the proof, and the pilot runs on whichever two projects are live.
5. **Savings arrive late**, because steel is bought before the nest exists. I track gain at purchase, and we agree in week 1 who books it.
6. **My rupee assumptions are wrong.** Appendix B shows the range and week 1 replaces them with the client's ledger.

**What I did not trust in the notes.**

| Claim | Why I did not trust it |
|---|---|
| "Automatic nesting wastes more" | It comes from the team that nests by hand, relayed second-hand by someone who says he sees nesting "from the outside," and nobody has measured it |
| "Offcuts are not used as well as they could be" | Same second-hand vantage. The rule already works; the instrument does not exist |
| "Utilisation is very low" | Severity without a number, and the client has not used six months of the data himself |
| "Overall 7 to 10%" | The basis is unstated, so I use it as a range and never as a baseline. It is consistent with the plate and profile rates for any plate share up to 33.3% |
| 80,000 t a year against 7,000 to 8,000 t a month | These disagree by up to 20%. I flagged them and used the annual figure |
| "Material cost cannot be split across projects" | The contact said he was unsure and would check with his team. I treat it as unconfirmed and build nothing on it |
| "Revision losses can be claimed back" | The contractual conditions are unknown, so I count only 25% as recoverable |
| An average project size | I can derive 5,333 t as 80,000 over 15 projects, but an average over an unknown distribution of project sizes is not a project size. I do not use it for pricing |

## 10) What did you use AI for? Which tools, where they helped, where they misled you, and what you threw away.

**Tools.** Claude for structure, drafting and adversarial challenge. Python to check every figure in the case study. A four-dimension self-eval harness to score the draft against the submission form before I read it as prose.

**Where it helped.** Ranking the six areas and separating "what they asked" from "what they need" came faster from the model than from my own reading, and it is the part of the structure that survived unchanged. The rejection list in section 3.3 was largely drafted and then pruned by me.

**Where it misled me. Three concrete errors it produced, all of which I caught by checking rather than reading.**

1. **It inverted the offcut question, and I nearly shipped it.** An early draft treated cross-project material reuse as blocked by cost loading and quoted "cost loads to the project that bought it" as the reason. I reread the notes: the client says "When they nest new projects, they check the offcuts first to see if anything can be used." Offcuts already cross projects. The blocked thing is sharing one *purchased plate*, which the client explicitly went to check. Conflating the two would have removed the largest value pool from my own case and mis-stated a client constraint to their face.
2. **It tested one edge of the wastage band instead of testing for overlap.** The draft asked whether the band's upper bound fell at or below 10%, found no solution, and concluded the client's figures were impossible. That would have told a fabricator their own numbers were wrong on our first call. The correct test is whether the bands overlap, which holds for every plate share up to 33.3%. Check: at plate share 15%, plate 20% and profiles 5%, the weighted overall is 0.15(20) + 0.85(5) = 3.00 + 4.25 = 7.25%, inside their stated 7 to 10%.
3. **It put cause codes in the wrong week.** The ledger design assigned revision-driven and error-driven waste to start filling in week 7, but the gate is week 4, which meant the baseline I was measuring against would have been incomplete at the moment I needed it. Cause codes now go in during week 3.

**What I threw away.** An outside steel price and an industry-typical nesting gain that were presented as findings rather than assumptions. A 6-week live trial that cut every nest twice, which doubles steel consumption and needs live projects this client may not have. A statistical margin I could not justify from the data the client actually has. An average-project-size figure I had derived and then realised was an average over an unknown distribution.

I kept the steel price as a labelled assumption in Appendix A, because the task requires a rupee value and the client can replace the number in week 1. The difference between a labelled assumption and an unlabelled one is the whole difference between this and the first draft.

## 11) Github Repo URL

The repository for this submission has been created alongside the three documents. It contains:

| Path | Contents |
|---|---|
| `README.md` | How to read the three deliverables, and which section of the case study answers which form question |
| `docs/case-study.md` | The case study |
| `docs/client-note.md` | The one-page note to the client contact |
| `docs/submission-form.md` | This form |
| `analysis/value_model.py` | Every rupee figure in sections 5 and 7, computed from the assumptions register. Prints the waste band, the crossover bounds, the cost build-up, the margin, all three value scenarios, payback and break-even |
| `analysis/wastage_check.py` | The band reconciliation and crossover at any plate share, with a regression test asserting the client's stated 7 to 10% is reachable for every plate share up to 33.3% |
| `tests/test_arithmetic.py` | Asserts 7,800 t and 9.75% at P = 15%, INR 33.08 lakh delivery cost, 39.9% margin, INR 1.46 crore conservative value and 4.5-month payback |

`tests/test_arithmetic.py` runs against `analysis/value_model.py` and must pass before submission. The arithmetic in the case study is not maintained by hand; it is generated from the assumptions register, so a changed assumption changes every downstream figure including the price case.

**On the prototype.** There is a working one at `prototype/index.html`, and it is deliberately not a nesting optimiser. It runs the actual deterministic packer from `analysis/packer.js` in the browser, lays the same 15 synthetic parts out under three capabilities, and lets you switch between them. `node tests/test_packer.js` asserts all 13 findings it displays, 13/13 passing.

It exists because building it changed my answer. I expected the Advisor's gain to come from nesting more tightly. It does not. On the plate in the prototype the software arms consume 380 mm less plate height than the hand nest and recover **exactly 0.000 t**, because the material saved comes back as a leftover nobody measures. Every recoverable tonne comes from registering the offcut. That is a sharper version of what the client told us, and it is the argument for widening the scope from "nesting optimisation" to material yield.

What the prototype does not prove: it is one synthetic plate, so it is a bug report and not a baseline. The replay still runs on 40 nests across 5 closed projects before anyone decides anything.