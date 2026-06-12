# JTBD and Prioritisation Table - Legacy-Trust Bank: Smart-Recovery Initiative

# 1. Grouping the Evidence

The following table groups all stakeholder evidence collected during Phase 1 discovery into six recurring themes. Confidence is rated:

- High — confirmed by both data and testimony
- Medium — confirmed by testimony alone
- Low — inferred from context

# Theme Definitions

|Theme                    |Description                                                                                                                            |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
|Duplicate Work           |Agents re-doing work that a single system of record would make redundant — structural, not behavioural                                 |
|Missed Follow-Up         |Recoverable accounts falling out of the funnel due to absent system prompting and unreliable handovers                                 |
|Poor Visibility          |No single real-time view of account status, activity history, or operational performance across the portfolio                          |
|Customer Friction.       |Customers unable to self-serve, repeating their situation across multiple channels, and unprotected if vulnerable                      |
|Financial Credibility    |Key financial figures are unaudited estimates or low-confidence projections requiring triangulation and sensitivity testing            |
|Change Resistance        |Agent scepticism, historical change fatigue, and pride in workarounds that could block adoption even if the portal is technically sound|

# Stakeholder Evidence Table

| Stakeholder           | Quote or Observation                               | Theme             | Business Impact                                 | Confidence           |
|:----------------------|:---------------------------------------------------|:------------------|:------------------------------------------------|:---------------------|
| Amina Rahman          | “Agents spend a surprising amount of time just     | Duplicate Work    | Agent capacity consumed by non-value work — no  | High                 |
|                       | checking whether someone else has already contacted|                   | account forward progress made during duplicate  |                      |
|                       | a customer that day or that week. We don’t have a  |                   | checks.                                         |                      |
|                       | reliable single view.” (Stakeholder interview)     |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Gareth Evans          | “There’s no automatic flag or lock on accounts, so | Duplicate Work    | Customers contacted multiple times by different | High                 |
|                       | honestly it comes down to scanning the notes column|                   | agents — damages customer trust and wastes      |                      |
|                       | and hoping your colleague remembered to timestamp  |                   | handling time on already-worked accounts        |                      |
|                       | their last attempt.” (Stakeholder interview)       |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Amina Rahman          | “The operational tracker is a monolithic           | Duplicate Work    | Every account action requires two system updates| High                 |
|                       | spreadsheet containing over 200 tabs. Every status |                   | — doubling administrative effort with no        |                      |
|                       | change in the primary database requires agents to  |                   | additional value created                        |                      |
|                       | manually re-key information into Excel.”           |                   |                                                 |                      |
|                       | (stakeholder_interview_notes.csv)                  |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Amina Rahman          | “Spreadsheet reconciliations and status checks     | Duplicate Work    | 34.2% of all operational hours spent on         | High                 |
|                       | absorb a massive portion of operational hours —    |                   | back-office admin rather than customer contact, |                      |
|                       | agents are doing work that a decent system should  |                   | confirmed by activity tracker sampling          |                      |
|                       | handle automatically.” (Stakeholder interview)     |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Amina Rahman          | “We don’t have automated prompts or a proper queue | Missed Follow-Up  | Recoverable accounts fall out of the funnel     | High                 |
|                       | — agents are expected to remember or manually check|                   | entirely — directly contributing to the 14%     |                      |
|                       | which accounts need follow-up and when. So even    |                   | missed touchpoint rate confirmed by finance     |                      |
|                       | when workload is manageable, things slip through.” |                   |                                                 |                      |
|                       | (Stakeholder interview)                            |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Amina Rahman          | “There’s a handover process on paper, but in       | Missed Follow-Up  | ~20% of follow-ups lost entirely at shift       | High                 |
|                       | practice it’s patchy. Continuity really does depend|                   | handovers — promise commitments broken with     |                      |
|                       | on individual diligence. It’s one of those         |                   | no system record of the failure                 |                      |
|                       | problems that’s invisible until a customer calls   |                   |                                                 |                      |
|                       | back frustrated.” (Stakeholder interview)          |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Gareth Evans          | “The legacy system lets you set a callback date,   | Missed Follow-Up  | 643 accounts confirmed stuck in Awaiting        | High                 |
|                       | but it’s purely informational — there’s no workflow|                   | Follow-Up with no automated prompt to surface   |                      |
|                       | trigger that surfaces the account again or alerts  |                   | them (delinquent_accounts_sample.csv)           |                      |
|                       | anyone when the date passes.” (Stakeholder         |                   |                                                 |                      |
|                       | interview)                                         |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Daniel Okoye          | “Finance estimates that 14% of collection files    | Missed Follow-Up  | 14% of £8M monthly baseline = ~£1.12M/month     | High                 |
|                       | currently suffer from delayed or entirely missed   |                   | in recoverable revenue leaking from the         |                      |
|                       | touchpoints due to existing process friction.”     |                   | portfolio due to missed agent touchpoints       |                      |
|                       | (finance_assumptions_sample.csv)                   |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Gareth Evans          | “When an account hits the queue, the first thing   | Poor Visibility   | Two-system check required before any productive | High                 |
|                       | most agents do is pull up the legacy database to   |                   | action — structural inefficiency built into     |                      |
|                       | see the balance and status, then immediately flip  |                   | every single account interaction                |                      |
|                       | over to the shared spreadsheet tracker.”           |                   |                                                 |                      |
|                       | (Stakeholder interview)                            |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Daniel Okoye          | “Audit trails are scattered across email,          | Poor Visibility   | Leadership cannot accurately forecast recovery  | High                 |
|                       | standalone spreadsheets, and a 20-year-old         |                   | yields or identify where the process is         |                      |
|                       | database. Reporting is meaningless because status  |                   | breaking — strategic blindspot at portfolio     |                      |
|                       | codes mean different things to different teams.”   |                   | level                                           |                      |
|                       | (stakeholder_interview_notes.csv)                  |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Daniel Okoye          | “The 38% figure is deliberately conservative — it  | Poor Visibility   | Without reliable status data, eligibility       | Medium               |
|                       | factors in expected customer dropout, channel      |                   | modelling requires large conservative buffers,  |                      |
|                       | preference, and a buffer for underlying complexity |                   | reducing the apparent addressable opportunity   |                      |
|                       | not visible in the sample.” (Stakeholder interview)|                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Daniel Okoye          | “69 accounts carry no status at all — Missing or   | Poor Visibility   | 69 unassigned accounts represent a compliance   | High                 |
|                       | Unassigned. Accounts are distributed evenly across |                   | gap — no recovery action can be reliably taken  |                      |
|                       | operational milestones with a heavy skew toward    |                   | or audited on these cases                       |                      |
|                       | follow-ups.” (delinquent_accounts_sample.csv)      |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Amina Rahman          | “Customers have to call in because they do not     | Customer Friction | 3 agent-handled calls per resolution for cases  | Medium               |
|                       | realise online payment is an option, leading to    |                   | that could self-serve — multiplied across       |                      |
|                       | repeating their vulnerable situations across       |                   | thousands of eligible accounts this is          |                      |
|                       | multiple transfers — 3 calls on average.”          |                   | substantial operational waste                   |                      |
|                       | (stakeholder_interview_notes.csv)                  |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Gareth Evans          | “From scratch, unfortunately. If someone’s been    | Customer Friction | Customers repeat information across every       | High                 |
|                       | through the app or the phone menu first, we don’t  |                   | channel transfer — extending resolution time    |                      |
|                       | see any of that journey when they land with us.    |                   | and damaging the customer experience            |                      |
|                       | The call just comes through and we’re starting     |                   |                                                 |                      |
|                       | fresh.” (Stakeholder interview)                    |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Gareth Evans          | “Honestly, recognition is mostly down to experience| Customer Friction | FCA vulnerable customer guidance at risk —      | High                 |
|                       | and gut instinct. There’s no flag in the system    |                   | legacy system treats routine delinquencies and  |                      |
|                       | that says this is a vulnerable customer unless     |                   | severe hardship cases identically, introducing  |                      |
|                       | someone’s manually added a note previously.”       |                   | high regulatory exposure                        |                      |
|                       | (Stakeholder interview)                            |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Gareth Evans          | “The escalation is manual — it’s an email to a     | Customer Friction | Vulnerable customers may not reach specialist   | High                 |
|                       | shared inbox with the account details and context. |                   | support reliably — no formal handoff workflow   |                      |
|                       | There’s no formal handoff workflow, so the agent   |                   | means compliance and reputational risk          |                      |
|                       | often ends up checking back to make sure it        |                   |                                                 |                      |
|                       | landed.” (Stakeholder interview)                   |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Daniel Okoye          | “Both the plan selection uplift (+4%) and promise  | Financial         | Without a sensitivity range the entire business | High                 |
|                       | capture uplift (+2.5%) are marked low confidence,  | Credibility       | case is vulnerable to board challenge — these   |                      |
|                       | yet they drive over 90% of the financial upside.   |                   | two assumptions drive 90%+ of the upside        |                      |
|                       | Absolutely build a sensitivity matrix.”            |                   |                                                 |                      |
|                       | (Stakeholder interview)                            |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Daniel Okoye          | “That £500,000 figure isn’t something finance has  | Financial         | Unverified headline figure creates model        | High                 |
|                       | formally validated. It likely came from Amina’s    | Credibility       | vulnerability — board will ask where it comes   |                      |
|                       | team as an operational estimate. Use it, but caveat|                   | from and if unanswered the case gets discredited|                      |
|                       | it explicitly and triangulate it.”                 |                   |                                                 |                      |
|                       | (Stakeholder interview)                            |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Daniel Okoye          | “I’d want additional evidence before we attribute  | Financial         | Overclaiming portal attribution without         | High                 |
|                       | that reduction directly to the portal. The 14%     | Credibility       | measurement infrastructure undermines the       |                      |
|                       | missed follow-up rate has multiple causes — agent  |                   | Phase 2 funding case before it is even made     |                      |
|                       | workload, prioritisation, system latency.”         |                   |                                                 |                      |
|                       | (Stakeholder interview)                            |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Daniel Okoye          | “A medium-complexity deployment of £85,000         | Financial         | Payback horizon is less than 9 days even at     | High                 |
|                       | represents less than 9 days of the cash upside     | Credibility       | base assumptions — the single most powerful     |                      |
|                       | generated by a 4% recovery plan selection uplift   |                   | number in the business case for leadership      |                      |
|                       | at £320,000/month.”(finance_assumptions_sample.csv)|                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Gareth Evans          | “The biggest pushback would be around flexibility  | Change Resistance | Portal adoption fails if agents route complex   | High                 |
|                       | for edge cases. The workarounds exist because the  |                   | cases around it — self-fulfilling prophecy that |                      |
|                       | official process doesn’t handle every situation    |                   | the system cannot handle real work, reducing    |                      |
|                       | cleanly.” (Stakeholder interview)                  |                   | actual efficiency gains                         |                      |
|                       |                                                    |                   |                                                 |                      |
| Gareth Evans          | “Some agents take real pride in managing their own | Change Resistance | Partial adoption reduces efficiency gains and   | High                 |
|                       | patch of accounts and knowing those customers’     |                   | makes before/after performance measurement      |                      |
|                       | histories. If a new system feels like it’s taking  |                   | unreliable — undermining the Phase 2 case       |                      |
|                       | that autonomy away, you’ll get resistance.”        |                   |                                                 |                      |
|                       | (Stakeholder interview)                            |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Amina Rahman          | “Teams are deeply hesitant to try new software     | Change Resistance | Historical change fatigue means agents will     | High                 |
|                       | tools because they feel they were burned by a      |                   | scrutinise Phase 1 launch closely — any early   |                      |
|                       | failed, disruptive system update five years ago    |                   | failure will entrench scepticism and damage     |                      |
|                       | that leadership approved and then abandoned.”      |                   | Phase 2 prospects                               |                      |
|                       | (stakeholder_interview_notes.csv)                  |                   |                                                 |                      |
|                       |                                                    |                   |                                                 |                      |
| Amina Rahman          | “Because the system is built on these unwritten    | Change Resistance | Tribal knowledge dependency makes               | Medium               |
|                       | tribal workarounds and an unstable spreadsheet     |                   | standardisation appear threatening to           |                      |
|                       | grid, it takes a new agent an extra two weeks just |                   | experienced agents — resistance is structural   |                      |
|                       | to reach basic productivity.”                      |                   | not personal                                    |                      |
|                       | (stakeholder_interview_notes.csv)                  |                   |                                                 |                      |

# Evidence Summary by Theme

|Theme                |Evidence Rows|Strongest Single Data Point                                                           |
|---------------------|-------------|--------------------------------------------------------------------------------------|
|Duplicate Work       |4            |72.3% spreadsheet reconcile duplicate rate; 0% duplication in all other activity types|
|Missed Follow-Up     |4            |14% missed touchpoints = ~£1.12M/month at risk (finance_assumptions_sample.csv)       |
|Poor Visibility      |4            |69 accounts with no status; status codes mean different things across teams           |
|Customer Friction    |4            |Avg 3 calls per resolution; zero cross-channel context; no vulnerability flagging     |
|Financial Credibility|4            |Both uplift assumptions low confidence yet drive 90%+ of upside                       |
|Change Resistance    |4            |Failed update 5 years ago; tribal workarounds take 2 extra weeks to teach new starters|

# 2. Jobs-to-be-Done Statements

The following JTBD statements are drawn from two sources: the Gemini Gem output (which processed stakeholder interview notes) and direct stakeholder testimony collected during Phase 1 discovery.

Statements are grouped by persona and linked back to the original evidence that inspired them.

## JTBD-01 — Customer

**When** I fall into past-due status and need to resolve my outstanding debt,
**I want** to have clear, self-service control over my account balance and payment options,
**so that** I can manage my financial obligations privately without the anxiety of a manual collections call.

|Field              |Detail                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------|
|**Source**         |Amina Rahman — "Customers don't realise online payment is an option, leading to repeating their     |
|                   |vulnerable situations across multiple transfers — averaging 3 calls to resolve a single query."     |
|                   |(stakeholder_interview_notes.csv)                                                                   |
|                   |                                                                                                    |
|**Confidence**     |High                                                                                                |
|                   |                                                                                                    |
|**Business Impact**|If left unmet, repayment rates drop because customers avoid contact due to anxiety, driving up      |
|                   |operational call volumes for straightforward enquiries that could self-serve                        |


## JTBD-02 — Customer

**When** I receive a complex update regarding my payment plan over the phone,
**I want** to easily access an accurate permanent record of what was agreed,
**so that** I don’t have to repeatedly call back to confirm the details.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Gareth Evans — "From scratch, unfortunately. If someone's been through the app or the phone menu  |
|                   |first, we don't see any of that journey when they land with us." (Stakeholder interview)          |
|                   |                                                                                                  |
|**Confidence**     |High                                                                                              |
|                   |                                                                                                  |
|**Business Impact**|Failure to meet this job results in inflated repeat call volumes and severe customer frustration  |
|                   |due to inconsistent records across disconnected systems                                           |


## JTBD-03 — Collections Agent

**When** I log in to start my shift,
**I want** to be automatically guided to the highest-priority customer accounts in a strategic sequence,
**so that** I am maximising my recovery efforts rather than guessing who to call next.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Amina Rahman — "It's less a deliberate policy and more that we never built the infrastructure to  |
|                   |do it differently. The legacy system doesn't score accounts or prioritise queues — it just shows  |
|                   |you a list." (Stakeholder interview)                                                              |
|                   |                                                                                                  |
|**Confidence**     |High                                                                                              |
|                   |                                                                                                  |
|**Business Impact**|Without this, agents waste valuable contact time on low-probability accounts, leaving high-risk   |
|                   |debt unaddressed and recovery yields below potential                                              |


## JTBD-04 — Collections Agent

**When** a customer requests a specific follow-up date,
**I want** the system to strictly enforce that callback schedule,
**so that** I never lose track of a hot lead or break a promise to a customer.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Gareth Evans — "The legacy system lets you set a callback date, but it's purely informational —   |
|                   |there's no workflow trigger that surfaces the account again or alerts anyone when the date passes."|
|                   |(Stakeholder interview)                                                                           |
|                   |                                                                                                  |
|**Confidence**     |High                                                                                              |
|                   |                                                                                                  |
|**Business Impact**|Accounts get permanently stuck in pending limbo — 643 confirmed in Awaiting Follow-Up — causing   |
|                   |broken negotiation loops and lost recovery revenue                                                |


## JTBD-05 — Collections Agent

**When** I log the outcome of a customer interaction,
**I want** to select from standardised, mutually exclusive status codes,
**so that** the history of the account is perfectly clear to anyone who inherits the case.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Daniel Okoye — "Audit trails are scattered across email, standalone spreadsheets, and a 20-year-  |
|                   |old database. Reporting is meaningless because status codes mean different things to different    |
|                   |teams." (stakeholder_interview_notes.csv)                                                         |
|                   |                                                                                                  |
|**Confidence**     |High                                                                                              |
|                   |                                                                                                  |
|**Business Impact**|Total breakdown of operational reporting accuracy and chaotic account handovers — confusing a     |
|                   |promise with a confirmation creates downstream compliance and recovery failures                   |


## JTBD-06 — Collections Agent

**When** I am negotiating a complex repayment plan,
**I want** the autonomy to apply compliant, flexible solutions that match the customer’s actual hardship,
**so that** I can resolve the case effectively without being blocked by rigid system constraints.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Gareth Evans — "The biggest pushback would be around flexibility for edge cases. The workarounds  |
|                   |exist because the official process doesn't handle every situation cleanly." (Stakeholder interview)|
|                   |                                                                                                  |
|**Confidence**     |Medium                                                                                            |
|                   |                                                                                                  |
|**Business Impact**|High agent attrition and burnout driven by systemic frustration, alongside a drop in first-contact|
|                   |resolution rates for complex cases                                                                |


## JTBD-07 — Operations Manager

**When** a new debt collection case enters the operation,
**I want** it instantly routed to the correct specialist queue based on its complexity and risk profile,
**so that** it can be resolved efficiently rather than bottlenecking behind unrelated cases for days.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Amina Rahman — "Accounts are contacted in a completely random order rather than a strategic       |
|                   |sequence. Simple cases get queued behind complex, slow-moving files, dragging down overall        |
|                   |recovery velocities." (stakeholder_interview_notes.csv)                                           |
|                   |                                                                                                  |
|**Confidence**     |High                                                                                              |
|                   |                                                                                                  |
|**Business Impact**|Simple cases escalate in cost and duration, artificially inflating the size of active queues and  |
|                   |delaying cash flow recovery                                                                       |


## JTBD-08 — Operations Manager

**When** a regulatory compliance audit occurs,
**I want** to access a unified, chronological history of all customer interactions across all channels,
**so that** we can pass reviews instantly without stitching together disjointed spreadsheets and emails.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Daniel Okoye — "Audit trails are scattered across email, standalone spreadsheets, and a 20-year-  |
|                   |old database. Status codes mean different things to different teams."                             |
|                   |(stakeholder_interview_notes.csv)                                                                 |
|                   |                                                                                                  |
|**Confidence**     |High                                                                                              |
|                   |                                                                                                  |
|**Business Impact**|Legacy-Trust faces severe regulatory risk, compliance audit failures, and massive operational     |
|                   |drain during look-back reviews without a unified audit trail                                      |


## JTBD-09 — Finance Partner

**When** verifying monthly recovery performance,
**I want** transactional agent activity logs to automatically reconcile with the core database balances,
**so that** we don’t have to spend days manually hunting for variances.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Daniel Okoye — "Hard savings are defensible with operational data. Revenue uplift is inherently   |
|                   |speculative until you've got real portal performance to measure." (Stakeholder interview)         |
|                   |                                                                                                  |
|**Confidence**     |High                                                                                              |
|                   |                                                                                                  |
|**Business Impact**|Extended financial close cycles, lack of trust in operational data, and leakage of unreconciled   |
|                   |cash positions that distort the ROI case                                                          |


## JTBD-10 — Finance Partner

**When** allocating collection resources,
**I want** to differentiate between customers who are genuinely unable to pay due to hardship and those who are avoiding contact,
**so that** we can apply tailored forbearance strategies legally and ethically.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Gareth Evans — "Honestly, recognition is mostly down to experience and gut instinct. There's no   |
|                   |flag in the system that says this is a vulnerable customer." (Stakeholder interview) + Daniel     |
|                   |Okoye — "If Phase 1 can introduce even basic vulnerability flagging, that strengthens the business|
|                   |case beyond efficiency savings — it becomes a risk mitigation play." (Stakeholder interview)      |
|                   |                                                                                                  |
|**Confidence**     |High                                                                                              |
|                   |                                                                                                  |
|**Business Impact**|Legacy-Trust risks treating vulnerable customers aggressively, violating FCA forbearance rules and|
|                   |harming brand reputation                                                                          |


## JTBD-11 — Team Leader

**When** my agents are struggling with high-friction workflows,
**I want** to secure modern operational tooling that eliminates duplicated admin rather than replacing agent judgement,
**so that** I can protect team morale and reduce the costly attrition of experienced staff.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Gareth Evans — "Any standardisation needs to show it's making their judgement easier to apply, not|
|                   |replacing it. If the system feels like it removes autonomy, you'll get resistance even if the tool|
|                   |is objectively better." (Stakeholder interview)                                                   |
|                   |                                                                                                  |
|**Confidence**     |Medium                                                                                            |
|                   |                                                                                                  |
|**Business Impact**|Continued loss of top-performing collection agents to competitors, leading to high recruitment    |
|                   |overhead and lower overall department performance                                                 |


## JTBD-12 — Product Manager

**When** migrating workflows to a digital-first ecosystem,
**I want** a unified single view of the customer across all legacy entry points,
**so that** our technical architecture does not fragment the customer journey or create conflicting outreach.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Priya Nair — "If someone asks why did we do it this way in three months, the answer shouldn't be  |
|                   |'I think Ross said something in a call.' This is the traceback I keep mentioning." (Stakeholder   |
|                   |interview) + Gareth Evans — "Collections sits apart from the main customer service platform —     |
|                   |there's no shared view of the interaction history." (Stakeholder interview)                       |
|                   |                                                                                                  |
|**Confidence**     |High                                                                                              |
|                   |                                                                                                  |
|**Business Impact**|Duplicate accounts remain in the database, leading to conflicting outreach strategies, broken     |
|                   |portal experiences, and corrupted reporting metrics                                               |


## JTBD-13 — Product Manager

**When** launching self-service debt resolution tools,
**I want** an immediate automated trigger that safely routes contested balances or vulnerable customers to human specialists,
**so that** we protect the customer’s rights while maintaining legal compliance.

|Field              |Detail                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------|
|**Source**         |Gareth Evans — "The escalation is manual — it's an email to a shared inbox. There's no formal     |
|                   |handoff workflow, so the agent often ends up checking back to make sure it's been picked up."     |
|                   |(Stakeholder interview)                                                                           |
|                   |                                                                                                  |
|**Confidence**     |Medium                                                                                            |
|                   |                                                                                                  |
|**Business Impact**|Without automated escalation guardrails, the portal risks breaching FCA vulnerable customer       |
|                   |guidance and exposing Legacy-Trust to regulatory enforcement action                               |


# Step 3: Prioritise the Unmet Jobs

Each JTBD statement is ranked High / Medium / Low across three dimensions:

- **Frequency of Evidence** — how often this need appeared across datasets and stakeholder interviews
- **Business Impact** — the measurable consequence if this job stays unmet
- **Portal Relevance** — how directly Phase 1 portal scope can address this job

-----

## JTBD Prioritisation Table

|JTBD ID|Actor             |Statement (summary)                                          |Evidence Frequency|Business Impact|Portal Relevance|Priority|
|-------|------------------|-------------------------------------------------------------|------------------|---------------|----------------|--------|
|JTBD-01|Customer          |Resolve debt privately via self-service without a collections|High              |High           |High            |HIGH    |
|       |                  |call                                                         |                  |               |                |        |
|JTBD-02|Customer          |Access a permanent record of what was agreed on a call       |Medium            |Medium         |Medium          |MEDIUM  |
|JTBD-03|Collections Agent |Be guided to highest-priority accounts automatically at      |High              |High           |Medium          |HIGH    |
|       |                  |shift start                                                  |                  |               |                |        |
|JTBD-04|Collections Agent |System enforces callback dates so no follow-up is ever lost  |High              |High           |High            |HIGH    |
|JTBD-05|Collections Agent |Log outcomes using standardised status codes understood      |High              |High           |High            |HIGH    |
|       |                  |by all teams                                                 |                  |               |                |        |
|JTBD-06|Collections Agent |Apply flexible, compliant solutions for complex cases        |Medium            |Medium         |Low             |MEDIUM  |
|       |                  |without rigid constraints                                    |                  |               |                |        |
|JTBD-07|Operations Manager|Route new cases instantly to the correct specialist queue    |High              |High           |Medium          |HIGH    |
|       |                  |by complexity                                                |                  |               |                |        |
|JTBD-08|Operations Manager|Access unified audit trail across all channels for compliance|High              |High           |Low             |MEDIUM  |
|       |                  |reviews                                                      |                  |               |                |        |
|JTBD-09|Finance Partner   |Activity logs auto-reconcile with database balances monthly  |Medium            |High           |Low             |MEDIUM  |
|JTBD-10|Finance Partner   |Differentiate hardship customers from avoidance to apply     |High              |High           |High            |HIGH    |
|       |                  |correct forbearance strategy                                 |                  |               |                |        |
|JTBD-11|Team Leader       |Secure modern tooling that eliminates admin without          |Medium            |Medium         |Medium          |MEDIUM  |
|       |                  |replacing agent judgement                                    |                  |               |                |        |
|JTBD-12|Product Manager   |Unified single customer view across all legacy entry points  |Medium            |High           |Medium          |MEDIUM  |
|JTBD-13|Product Manager   |Automated trigger routes contested or vulnerable cases       |High              |High           |High            |HIGH    |
|       |                  |to human specialists                                         |                  |               |                |        |


## Priority Summary

|Priority|JTBD IDs                                                     |Count|
|--------|-------------------------------------------------------------|-----|
|HIGH    |JTBD-01, JTBD-03, JTBD-04, JTBD-05, JTBD-07, JTBD-10, JTBD-13|7    |
|MEDIUM  |JTBD-02, JTBD-06, JTBD-08, JTBD-09, JTBD-11, JTBD-12         |6    |
|LOW     |None                                                         |0    |


> No statements were ranked Low. Every identified job has meaningful business impact.
> The distinction between High and Medium is driven primarily by portal relevance
> Medium jobs are real needs but either require infrastructure beyond Phase 1 scope or depend on Phase 2 technical work to address properly.


# Top 3 Unmet Jobs — Detailed Justification


## #1 — JTBD-04: Collections Agent — Enforced Callback Scheduling

**Statement:**
“When a customer requests a specific follow-up date, I want the system to strictly enforce that callback schedule, so that I never lose track of a hot lead or break a promise to a customer.”

### Why It Matters Now

This is the single most damaging operational failure in the current process. Callback dates exist in the legacy system but are purely informational — no trigger fires when a date passes, and no account is surfaced automatically. The consequence is visible in the data: 643 accounts are confirmed stuck in Awaiting Follow-Up, the largest single status backlog in the portfolio. Gareth Evans confirmed this is a known, longstanding problem that IT previously attempted and deprioritised. Amina Rahman identified the absence of automated prompting as the root cause of the backlog — not agent capacity.

### Evidence Supporting It

- 643 accounts in Awaiting Follow-Up status (delinquent_accounts_sample.csv)
- Finance estimates 14% of collection files suffer missed or delayed touchpoints (finance_assumptions_sample.csv)
- ~20% of follow-ups lost entirely at shift handovers (Amina Rahman, stakeholder interview)
- Gareth Evans confirmed callback enforcement was raised with IT and never delivered (Stakeholder interview)

### How It Influences Phase 1 Scope

Automated callback triggering is confirmed as a Phase 1 requirement. It is technically self-contained — it does not require platform integration or eligibility rule changes. It directly addresses the 14% missed touchpoint rate that finance uses as the cost-of-inaction benchmark. Fixing this alone partially validates the portal’s value case within the first 90 days of launch, supporting the Phase 1 to Phase 1b transition measurement framework.


## #2 — JTBD-01: Customer — Self-Service Debt Resolution Without a Collections Call

**Statement:**
“When I fall into past-due status and need to resolve my outstanding debt, I want to have clear self-service control over my account balance and payment options, so that I can manage my financial obligations privately without the anxiety of a manual collections call.”

### Why It Matters Now

This is the foundational job that the entire Smart-Recovery portal is built to serve. 77.5% of accounts in the sample are already technically eligible for self-service based on risk flag and delinquency stage alone — the demand side of the equation is confirmed by the data. The supply side is currently non-existent: customers do not know self-service is an option, averaging 3 calls to resolve a query that could be handled digitally. Every one of those calls consumes agent time that should be directed at complex and vulnerable cases.

### Evidence Supporting It

- 77.5% of accounts flagged as self-service eligible (delinquent_accounts_sample.csv)
- Customers average 3 calls per resolution — self-service awareness is near zero (stakeholder_interview_notes.csv)
- Eligibility is time-based not balance-based — early intervention is the highest-value window (delinquent_accounts_sample.csv)
- Finance plan selection uplift of +4% on £8M monthly baseline = £320,000/month if self-service successfully guides customers to repayment plans (finance_assumptions_sample.csv)

### How It Influences Phase 1 Scope

Promise-to-Pay is confirmed as the Phase 1 anchor journey — the lowest complexity self-service path with the clearest rules and highest conversion potential. This JTBD directly scopes the portal’s core customer-facing function. It also drives the Phase 1 notification requirement: agents verbally directing customers to the portal during calls as the initial awareness mechanism, with automated SMS/email notification deferred to Phase 1b once compliance approves messaging templates.


## #3 — JTBD-10: Finance Partner — Differentiate Hardship from Avoidance

**Statement:**
“When allocating collection resources, I want to differentiate between customers who are genuinely unable to pay due to hardship and those who are avoiding contact, so that we can apply tailored forbearance strategies legally and ethically.”

### Why It Matters Now

This job sits at the intersection of operational efficiency, financial credibility, and regulatory compliance — making it uniquely high-priority across all three ranking dimensions. The current system treats routine delinquencies and severe hardship cases identically. There is no system flag for vulnerability. Gareth Evans confirmed recognition is entirely gut instinct during calls. Daniel Okoye confirmed this is a real FCA regulatory risk — firms must identify and respond appropriately to customers showing signs of financial difficulty or vulnerability. If Phase 1 can introduce even basic vulnerability flagging or routing logic, Daniel stated it strengthens the business case beyond efficiency savings into risk mitigation — which carries additional weight with leadership.

### Evidence Supporting It

- No vulnerability flag exists in the legacy system — recognition is gut instinct
  (Gareth Evans, stakeholder interview)
- Hardship escalation is a manual email to a shared inbox with no formal handoff
  (Gareth Evans, stakeholder interview)
- FCA guidance on vulnerable customers is clear — firms must identify and respond appropriately (Daniel Okoye, stakeholder interview)
- Daniel confirmed vulnerability routing strengthens the Phase 1 business case as risk mitigation, not just efficiency (Stakeholder interview)

### How It Influences Phase 1 Scope

Vulnerability escalation path with full context handoff to a specialist queue is confirmed as a Phase 1 requirement. The portal must provide a clear and easy escalation route at every decision point. When a customer self-identifies as in hardship or the system detects risk indicators, the portal must extract them from the automated sequence and pass full interaction context to a specialist agent — not a general queue. This is both a UX requirement and a compliance requirement. The formal FCA exposure assessment from the risk team remains an open action before Phase 1 launch.
