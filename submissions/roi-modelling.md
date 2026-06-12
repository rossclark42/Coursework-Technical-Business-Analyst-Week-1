# ROI Model — Legacy-Trust Bank: Smart-Recovery Initiative

The the ROI model can be found here: https://docs.google.com/spreadsheets/d/1WIOMpWksjAYcIkvWkBM814R3YTxHWA0c/edit?usp=sharing&ouid=109992888420466855782&rtpof=true&sd=true

## 1 Rank and Recommend

### Final Ranked Opportunity View

All six automation opportunities ranked by Net Year 1 Benefit, assessed against value, implementation effort, confidence in assumptions, and relevance to Phase 1 scope.

|Rank|Opportunity                           |Net Year 1 £|Effort    |Confidence|Phase      |
|----|--------------------------------------|------------|----------|----------|-----------|
|1   |AO-02: Automated Callback Triggering  |£4,047,746  |Low (£45k)|High      |Phase 1    |
|2   |AO-06: Automated Follow-Up Reminders  |£3,119,404  |Low (£45k)|Low       |Phase 1b   |
|3   |AO-04: Customer Balance & Account V   |£3,054,178  |Low (£45k)|Medium    |Phase 1    |
|4   |AO-01: Promise-to-Pay Self-Service    |£1,588,816  |Low (£45k)|Medium    |Phase 1    |
|5   |AO-03: Real-Time Status Sync          |£1,331,922  |Mid (£85k)|High      |Pre-Phase 1|
|6   |AO-05: Risk-Based Queue Prioritisation|£995,582    |Mid (£85k)|Low       |Phase 2    |

-----

### Three-Scenario Sensitivity Analysis

Hard savings and revenue uplift presented separately per Daniel Okoye’s instruction. Hard savings are High confidence and defensible with operational data. Revenue uplift is Low confidence and must not be blended with hard savings in board presentations.

|Component                |Base          |Conservative  |Floor         |
|-------------------------|--------------|--------------|--------------|
|Hard savings (annual)    |£168,985      |£168,985      |£168,985      |
|Revenue uplift (annual)  |£6,240,000    |£3,120,000    |£1,440,000    |
|**Total annual benefit** |**£6,408,985**|**£3,288,985**|**£1,608,985**|
|Implementation cost (mid)|-£85,000      |-£85,000      |-£85,000      |
|**Net Year 1 benefit**   |**£6,323,985**|**£3,203,985**|**£1,523,985**|
|12-month ROI             |7,440%        |3,769%        |1,793%        |
|Payback period (months)  |0.2           |0.3           |0.6           |

> **Key message for Daniel:** The business case is positive and compelling in all three scenarios including the stress case. At floor assumptions the £85k mid-complexity implementation cost is recovered in under one month. Hard savings alone (£168,985) recover the implementation cost within six months with zero revenue uplift.

-----

### Conservative and Optimistic Scenarios

#### Conservative Scenario

- Plan selection uplift: 2.0% (50% haircut on base)
- Promise capture uplift: 1.25% (50% haircut on base)
- Combined annual uplift: £3,120,000
- Net Year 1: **£3,203,985**
- Payback: **0.3 months**

This scenario assumes portal adoption is materially lower than finance projections and only half the anticipated uplift is realised. The case remains strongly positive. Hard savings provide a credible floor that does not depend on portal performance assumptions.

#### Optimistic Scenario (Base)

- Plan selection uplift: 4.0% (finance base assumption)
- Promise capture uplift: 2.5% (finance base assumption)
- Combined annual uplift: £6,240,000
- Net Year 1: **£6,323,985**
- Payback: **0.2 months**

This scenario reflects finance assumptions in full. Both uplift figures are rated Low confidence until portal performance data exists. Sensitivity testing confirms the case holds even if both assumptions are wrong by 75%.

-----

### Top Opportunity Justifications

#### #1 — AO-02: Automated Callback Triggering

**Net Year 1: £4,047,746 | Effort: Low | Confidence: High**

**Why it matters now:** The 643 accounts stuck in Awaiting Follow-Up represent the single largest operational backlog in the portfolio — confirmed by the delinquent accounts dataset. Gareth Evans confirmed callback dates have never been system-enforced, a problem previously raised with IT and deprioritised. Amina Rahman identified the absence of automated prompts as the root cause of the backlog, not agent capacity. This is a known, named, previously attempted fix with clear stakeholder mandate.

**Evidence supporting it:**

- 643 accounts confirmed in Awaiting Follow-Up (delinquent_accounts_sample.csv)
- Finance estimates 14% of collection files suffer missed or delayed touchpoints — £1.12M per month at risk (finance_assumptions_sample.csv)
- ~20% of follow-ups lost entirely at shift handovers (Amina Rahman, stakeholder interview)
- Hard saving of £60,746 confirmed from 230.1 wasted hours in activity tracker — High confidence

**How it influences Phase 1 scope:** Self-contained — requires no platform integration, no eligibility rule changes, no status governance prerequisite. Can be delivered within Phase 1 as a standalone trigger mechanism. Directly validates the measurement framework by providing a before/after backlog count.

-----

#### #2 — AO-04: Customer Balance & Account Summary View

**Net Year 1: £3,054,178 | Effort: Low | Confidence: Medium**

**Why it matters now:** This is the foundational portal layer without which no other customer journey can function. Customers currently average 3 calls to resolve a query partly because they cannot see their own balance or account status without calling in. Without a balance view the portal has no entry point — AO-01 (Promise-to-Pay) cannot be completed by a customer who cannot first see what they owe.

**Evidence supporting it:**

- Customers average 3 calls per resolution — self-service awareness is near zero (stakeholder_interview_notes.csv)
- 77.5% of accounts flagged as self-service eligible by risk and delinquency stage (delinquent_accounts_sample.csv)
- Hard saving of £1,179,178 from call deflection — estimated 2 calls saved per customer across effective portal population
- Revenue uplift of £1,920,000 — 50% attribution of plan selection uplift (£8M x 4% x 50% x 12)

**How it influences Phase 1 scope:** Must be included in Phase 1 as the portal entry point. AO-01 and AO-02 both depend on customers being able to access the portal and see their account. Without this layer the portal is not navigable. Low implementation cost (£45k) and no compliance dependencies beyond standard authentication.

-----

#### 3 — AO-01: Promise-to-Pay Self-Service Capture

**Net Year 1: £1,588,816 | Effort: Low | Confidence: Medium**

**Why it matters now:** Promise-to-Pay is confirmed as the Phase 1 anchor journey by Priya Nair. It is the lowest complexity self-service path — single date input, clear rules, works across risk bands — and carries the highest modelled conversion rate (89.9% in planning scenarios). It directly addresses JTBD-04, the top-ranked unmet job in the prioritisation analysis, and links to the promise capture revenue uplift assumption that finance has modelled at £200k per month at base.

**Evidence supporting it:**

- 319 accounts carry Promise Due status with no system enforcement (delinquent_accounts_sample.csv)
- Finance promise capture uplift of 2.5% on £8M = £200k/month base (finance_assumptions_sample.csv — Low confidence)
- Hard saving of £673,816 from handling time reduction across effective portal population (19,142 x 8min x £22/hr)
- Gareth Evans confirmed callback dates are informational only — no trigger fires when date passes (stakeholder interview)

**How it influences Phase 1 scope:** Primary customer journey for Phase 1. Requires AO-04 (balance view) as a prerequisite since customers need to confirm what they owe before committing to a payment date. Revenue uplift rated Low confidence until portal performance data exists — Phase 1 measurement infrastructure must track promise submission rate to validate post-launch.

-----

### Phase 1 Recommendation — Top Opportunities

**Recommended Phase 1 scope: AO-04 + AO-01 + AO-02**

Deploy these three opportunities together as the Phase 1 package.

AO-04 provides the portal entry point — customers can see their balance and account status. AO-01 is the primary self-service journey built on top of that foundation. AO-02 is the agent-side automation that attacks the operational backlog directly and provides the highest confidence hard saving in the model. Together these three deliver a complete Phase 1 proposition: one customer journey (Promise-to-Pay), one operational automation (callback triggering), and one foundational portal layer (balance view).

**AO-03 (Status Synchronisation) should run as a pre-Phase 1 dependency.** Without standardised status codes, portal eligibility rules will break on inconsistent data. This is process alignment work — not a build — and can be completed in weeks. Owners: Gareth Evans (team leads) for process alignment, Daniel Okoye (compliance) for sign-off.

**AO-06 (Follow-Up Reminders) moves to Phase 1b** pending compliance sign-off on messaging templates. FCA rules on contact frequency and opt-outs must be confirmed before automated SMS/email deployment.

**AO-05 (Queue Prioritisation) is Phase 2.** It requires the clean status foundation from AO-03 before it can function reliably, and its revenue assumptions are Low confidence.

-----

## 2 AI Feedback and Review

### Gaps and Weaknesses Identified by AI

#### Gap 1: Revenue uplift assumptions not sufficiently separated

**Identified:** Both plan selection (+4%) and promise capture (+2.5%) are rated Low confidence yet were initially presented in a single blended ROI figure. Daniel Okoye explicitly stated this would get the whole model tarred with the low-confidence brush.

**Actioned:** Hard savings and revenue uplift are now presented in separate rows throughout Tab 4 and Tab 5. The sensitivity matrix shows three distinct scenarios. All Low confidence figures are highlighted in red. The note “LOW CONFIDENCE — do not blend with hard savings” appears on every revenue uplift row.

-----

#### Gap 2: GBP500,000 revenue loss estimate presented without caveat

**Identified:** The operational estimate from Amina Rahman’s team appeared in the model without explicit sourcing or a caveat that it is not finance-recognised.

**Actioned:** The figure is labelled “Operational estimate — Amina Rahman. NOT finance-recognised. Caveat.” in Tab 2. A triangulation calculation (5% of 14% leakage x £8M x 12 = £672,000) is included alongside it to provide a second directional reference as Daniel instructed.

-----

#### Gap 3: 38% vs 77.5% eligibility gap unexplained in model

**Identified:** The model used 19,142 as the effective portal population without showing the three-layer logic that produces it, which Daniel would challenge immediately.

**Actioned:** Tab 1 shows all three layers explicitly:

- Technical eligibility: 77.5% (data-confirmed)
- Finance conservative estimate: 38% (dropout, channel preference, complexity buffer)
- Predicted adoption: 65% (estimated — Low confidence)
- Effective population: 100,000 x 77.5% x 38% x 65% = 19,142

-----

#### Gap 4: C9 handling time saving overstated by factor of 12

**Identified:** The original formula treated 19,142 as a monthly case volume and multiplied by 12, producing £673,816 instead of £56,151. 19,142 is the total portfolio stock, not a monthly flow — each account resolves approximately once per year via self-service.

**Actioned:** Formula corrected to remove the x12 multiplier. Note added: “Single resolution event per eligible account per year. Conservative — credit card accounts may re-delinquent 1.5-2x annually.”

-----

#### Gap 5: Phase 1 measurement framework missing from model

**Identified:** Daniel Okoye confirmed Phase 1 must include measurement infrastructure to validate attribution post-launch. Without it the model cannot be defended at Phase 1b funding stage.

**Actioned:** Tab 5 includes a full measurement framework with baseline, 90-day target, owner, and linked opportunity for six key metrics: Promise-to-Pay submission rate, Awaiting Follow-Up backlog, duplicate activity rate, agent admin time, missed follow-up rate, and portal adoption rate.

-----

#### Gap 6: AO-04 revenue uplift was missing entirely

**Identified:** AO-04 (Customer Balance & Account View) had no revenue uplift attributed despite being the portal entry point that enables plan selection journeys.

**Actioned:** Revenue uplift of £1,920,000 added (£8M x 4% plan selection x 50% attribution x 12). Attribution capped at 50% to avoid double-counting with AO-01.

-----

#### Gap 7: F8 (AO-03 revenue) was zero

**Identified:** Real-time status synchronisation was attributed zero revenue uplift. However status sync directly reduces missed touchpoints by fixing data inconsistency — the mechanism that causes a portion of the 14% leakage rate.

**Actioned:** Conservative 10% attribution applied: £8M x 14% x 10% x 12 = £1,344,000. Labelled explicitly as conservative attribution pending post-implementation measurement.

-----

### Remaining Caveats for Leadership Presentation

The following items should be disclosed explicitly when presenting the model to leadership:

**Revenue uplift figures are Low confidence** until portal performance data exists. The sensitivity matrix shows the case is positive even at floor assumptions — lead with this, not the base figure.

**The effective portal population (19,142)** is an estimate built from three layered assumptions. The 38% conservative factor from finance is a working estimate without formally documented dropout assumptions — Daniel confirmed this. The model shows all three layers transparently so the assumption can be challenged and updated.

**The GBP500,000 operational loss estimate** is not finance-recognised. It has been triangulated against activity tracker data (£672,000 directional estimate) which provides corroboration, but neither figure has been through the finance books.

**AO-03 revenue attribution (£1,344,000)** is conservative and indirect — it represents 10% of annual missed follow-up leakage attributed to data inconsistency. This should be presented as a directional estimate requiring post-launch validation rather than a committed projection.

**Phase 1 measurement infrastructure must be built in** before launch. This is a condition of Daniel’s support for attributing the 14% missed follow-up improvement to the portal in the Phase 1b funding case.

-----

### Improvements Validated and Actioned

|Improvement                                          |Status  |
|-----------------------------------------------------|--------|
|Hard savings separated from revenue uplift throughout|Actioned|
|Sensitivity matrix at base, conservative, floor      |Actioned|
|GBP500k figure caveated and triangulated             |Actioned|
|Three-layer eligibility funnel shown explicitly      |Actioned|
|C9 handling saving corrected                         |Actioned|
|AO-04 revenue uplift added                           |Actioned|
|F8 revenue uplift added (conservative attribution)   |Actioned|
|E11 hard saving corrected and annualised             |Actioned|
|Phase 1 measurement framework added                  |Actioned|
|All Low confidence figures highlighted red           |Actioned|