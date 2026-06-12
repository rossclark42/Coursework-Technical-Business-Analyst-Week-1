# Discovery Brief - Legacy-Trust Bank: Smart-Recovery Initiative

# 1. Problem Summary
Legacy-Trust Bank's debt recovery operation manages over 100,000 delinquent accounts across 58 agents using a 20-year-old legacy database, a 200-tab Excel tracker, and disconnected emails and phone systems. None communicate in real time. Operational sampling indicates more than 1 in 5 agent activities represent duplicated effort, with agents estimated t spend as little as 30-40% of their time on actual customer contact - the reminder absorbed by manual reconciliation, status checking, and re-keying data across systems. Finance estimates 14% of collection files suffer missed or delayed touch points, and the operational team attributes approximately £500,000 in lost annual recovery revenue to spreadsheet reliance. The current process cannot scale and the failure is systematic, not behavioural.

# Evidence
Duplicate rate is directional - drawn from a sample of 9,890 logged activities, not a portfolio-wide total. The 30-40% admin time estimate is sourced to Amina Rahman's direct testimony, independently supported by activity tracker sampling. The 14% missed touch point rate is from finance_assumptions_sample_csv. The £500,000 figure is an operational estimate from the Debt Recovery team - not finance recognised - and must be triangulated against activity tracker before use in the ROI model.

# Triangulation
Triangulation check on the £500,000 estimate: activity tracker data shows 1,465 activities with no follow-up date assigned, and 2,020 duplicate activities consuming 13,806 minutes of wasted agent time. Applying a conservative 5% attribution of the 14% missed follow-up leakage against the £8 million monthly baseline produces an annualized estimate of approximately £672,000 - directionally consistent with the £500,000 estimate.

# 2. Stakeholder Overview

| Stakeholder group     | What they care about    | How success is measured       | Main worry          | Evidence they will trust    |
|:----------------------|:------------------------|:------------------------------|:--------------------|:----------------------------|
| Operations leadership | Reducing wasted agent   | Clear map of where work breaks| Recommendations that| Activity tracker data       |
| (Amina Rahman)        | effort and restoring    | down, measurable reduction in | look clean on paper | duplicate rates, handling   |
|                       | visibility across       | duplicate outreach and missed | while operational   | time breakdown, and follow- |
|                       | 100,000+ accounts.      | follow-ups.                   | complexity still    | up loss rates.              |
|                       |                         |                               | lands on agents.    |                             |
|                       |                         |                               |                     |                             |
| Team leaders and      | Honest As-is documentat-| To-Be process that visibly    | A portal that looks | Process maps built from     |
| agents (Gareth Evans) | ation, future state     | handles edge cases and        | successful on paper | real workflow experience,   |
|                       | design that shows where | accommodates agent judgement  | while messy hand-   | change framing around       |
|                       | work starts and ends.   | rather than replacing it.     | offs and complex    | workload relief not job     |
|                       |                         |                               | cases still land    | replacement.                |
|                       |                         |                               | back on agents.     |                             |
|                       |                         |                               |                     |                             |
| Finance and Compliance| A defensible, evidence  | ROI model that holds under    | Transformation      | Layered eligibility funnel, |
| (Daniel Okoye)        | based value case with   | scrutiny with sensitivity     | numbers that do not | sensitivity matrix, figures |
|                       | transparent assumptions | testing at reduced uplift     | survive board       | triangulated across multiple|
|                       | and separated hard      | scenarios.                    | challenge,compliance| sources, hard-savings ring- |
|                       | savings from revenue    |                               | exposure from vulne-| fenced.                     |
|                       | uplift.                 |                               | rability flagging   |                             |
|                       |                         |                               | gap.                |                             |
|                       |                         |                               |                     |                             |
| Product and Delivery  | Traceable, buildable    | Four deliverable formats:     | Vague analysis that | Data-grounded analysis with |
| (Priya Nair)          | scope with clear links  | As-Is/To-Be maps, JTBD        | cannot be converted | documented scoping rationale|
|                       | from pain point to      | grounded user stories,        | into a backlog,scope| and a clear Phase 1 to Phase|
|                       | opportunity to          | log, assumptions register.    | decisions that get  | 1b transition trigger.      |
|                       | requirement.            |                               | re-litigated every  |                             |
|                       |                         |                               | week.               |                             |
|                       |                         |                               |                     |                             |
| Customers             | Resolve their debt      | Self-service completion       | Being pushed through| N/A - inferred from agent   |
|                       | situation quickly and   | without needed agent interven-| slow, repetitive    | testimony, interview notes  |
|                       | privately without       | tion, clear information about | contact journeys    | (avg 3 calls per resolution)|
|                       | friction and embarrass- | what they owe and their       | or bounced between  | and JTBD analysis.          |
|                       | ment of a collection    | options.                      | channels with no    |                             |
|                       | call.                   |                               | context carried over|                             |


# 3. Discovery Questions

1. Which steps in the debt recovery workflow are high-volume and rules-driven enough to be handled by self-service, and which genuinely require human judgement?
2. Where do spreadsheets and manual handoffs create duplicate work - and can that duplication be quantified in agent hours and revenue impact?
3. What baseline metrics demonstrate operational waste: duplicate contact rate, follow-up loss rate, admin-to-contact time ratio, or missed follow-up revenue leakage?
4. What is the strongest Phase 1 value case - agent time recovery from eliminating duplicate admin, or revenue uplift from automating promise capture and plan selection?
5. What would need to be true about data governance and status standardisation before a self-service portal could operate reliably?
6. Which customer journeys are suitable for self-service given the current eligibility gating logic, and what is the recoverable value within those boundaries?
7. What adoption and change management risks could block agent and customer uptake even if the portal is technically sound?

# 4. Traceability Starter

| Stakeholder concern            | Likely process area affected   | Possible metric or evidence    | Likely deliverable             |
|                                |                                | source                         |                                |
|:-------------------------------|:-------------------------------|:-------------------------------|:-------------------------------|  
| Agents duplicate outreach - no | Account assignment and status  | 20.4% duplicate rate, 230 hours| As-Is pain point, automated    |
| single view of who contacted an| management.                    | wasted - activity tracker.     | status sync in To-Be, ROI hard |
| account.                       |                                |                                | savings.                       |
|                                |                                |                                |                                |
| 643 accounts stuck in Awaiting | Follow-up scheduling and queue | 643 accounts confirmed -       | Phase 1 automation: automated  |
| Follow-Up with no system       | management.                    | delinquent_account data sample.| callback triggering requirement|
| prompt.                        |                                |                                |                                |
|                                |                                |                                |                                |
| 20% of follow-ups lost at shift| Shift handover and case        | Amina questioning + interview  | As-Is pain point, To-Be handoff|
| handovers.                     | ownership transfer.            | notes drop-off figure.         | design with digital ownership. |
|                                |                                |                                |                                |
| Agents spend only 30-40% of    | Account assignment and status  | Activity tracker 34.2% back-   | ROI model hard saving, ADKAR   |
| time on customer contact.      | management.                    | office, Amina questioning.     | message: workload relief not   |
|                                |                                |                                | job loss.                      |
|                                |                                |                                |                                |
| Status codes mean different    | Status management and data     | Daniel questioning, interview  | Pre-Phase 1: targeted Promise- |
| things across teams.           | governance.                    | notes SN-122, SN-085.          | to-Pay status standardisation. |
|                                |                                |                                |                                |
| No vulnerability flag in system| Case triage and routing.       | Gareth and Daniel questioning, | Phase 1 compliance requirement:|
| - FCA exposure.                |                                | FCA guidance reference.        | vulnerability escalation path. |
|                                |                                |                                |                                |
| Hardship escalation is manual  | Specialist case handoff.       | Gareth questioning - no formal | To-Be: formal escalation with  |
| email to shared inbox.         |                                | handoff workflow confirmed.    | full context handoff to        |
|                                |                                |                                | specialist queue.              |
|                                |                                |                                |                                |
| Zero cross-channel context     | Customer journey and agent     | Gareth questioning - collection| Phase 1 portal requirement:    |
| when customers transfer.       | handoff.                       | entirely separate from main    | context passing on escalation  |
|                                |                                | platform.                      | to agent.                      |
|                                |                                |                                |                                |
| 14% missed follow-up revenue   | End-to-End recovery funnel.    | Finance assumptions, 14% of £8m| ROI model cost-of-inaction     |
| leakage.                       |                                | = £1.2m/month.                 | benchmark, partial attribution |
|                                |                                |                                | to portal.                     |
|                                |                                |                                |                                |
| 38% vs 77.5% self-service      | Eligibility assessment and     | Daniel questioning, delinquent | ROI model, three layer funnel  |
| eligibility gap.               | case routing.                  | accounts self-service flag.    | - eligibility, adoption,       |
|                                |                                |                                | completion.                    |
|                                |                                |                                |                                |
| Customers unaware self-service | Customer contact and channel   | Interview notes JTBD, Priya    | Phase 1: agent verbal script,  |
| exists - avg 3 calls to resolve| strategy.                      | questioning.                   | Phase 1b: automated SMS/Email  |
|                                |                                |                                | notification.                  |

# 5. Final Problem Statement
Legacy-Trust's debt recovery operation is failing at scale because 58 agents are managing 100,000+ accounts across four disconnected systems with no single source of truth, no automated follow-up prompting, and no intelligent case routing. More than 1 in 5 agent activities is a duplicated effort, roughly 60-70% of agent time is absorbed by admin rather than customer contact, and 14% of collection files suffer missing or delayed touch points - leaking an estimated £1.2 million per month in recoverable revenue. The bank needs to identify which parts of this workflow are rules-driven enough to be automated or self-served, starting with promise-to-pay capture, prove the financial case with a transparent and sensitivity-tested ROI model, and design a portal that genuinely reduces agent workload rather than redistributing it.
