# Mapping the Process

## 1. Build the real current-state map

Full As-Is Process map to be found in submissions/Phase3_Coursework_As_Is.bpmn.

## 2. Mark where the workflow breaks

Pain points detailed on the As-Is Process map found in path above.

### Pain Point Register
#### PP-01: Duplicate Status Checks

**Stakeholder Quote:**

“Agents spend a surprising amount of time just checking whether someone else has already contacted a customer that day or that week. We don’t have a reliable single view, so people are cross-referencing spreadsheets, checking email threads, sometimes even asking around verbally before they dial.” — Amina Rahman (Stakeholder interview)

**Source Dataset:** recovery_activity_tracker_sample.csv

**Operational Observation:** 
Activity tracker sampling shows spreadsheet reconciliation carries a 72.3% duplicate rate across 1,458 activities, and status checking carries a 69.0% duplicate rate across 1,400 activities. All other activity types show a 0% duplication rate. This confirms duplication is structural — concentrated entirely in the two tasks that require agents to manually synchronise disconnected systems — not random agent behaviour.


#### PP-02: Missed and Delayed Follow-Up

**Stakeholder Quote:**

"We don't have automated prompts or a proper queue — agents are expected to remember or manually check which accounts need follow-up and when. So even when workload is manageable, things slip through because there's no reliable nudge." — Amina Rahman (Stakeholder interview)

**Source Dataset:** delinquent_accounts_sample.csv + finance_assumptions_sample.csv

**Operational Observation:** 643 accounts are confirmed stuck in Awaiting Follow-Up status — the largest single operational backlog category in the portfolio sample. Finance separately estimates that 14% of all collection files suffer delayed or entirely missed touchpoints due to process friction, representing approximately £1.12M per month in recoverable revenue at risk.


#### PP-03: Spreadsheet Reconciliation Waste

**Stakeholder Quote:**

"The operational tracker is now a monolithic spreadsheet containing over 200 tabs. Every status change in the primary database requires agents to manually re-key information into Excel." — Amina Rahman (stakeholder_interview_notes.csv)

**Source Dataset:** recovery_activity_tracker_sample.csv

**Operational Observation:** The activity tracker confirms 34.2% of all operational hours are spent on back-office admin tasks rather than customer contact. Spreadsheet reconciliation activities alone account for 9,411 minutes of wasted effort per sample period. This is the single largest category of non-contact agent work and is directly caused by the absence of real-time synchronisation between the legacy database and the spreadsheet tracker.


#### PP-04: Manual Promise-to-Pay Tracking

**Stakeholder Quote:**

"The legacy system lets you set a callback date, but it's purely informational — there's no workflow trigger that surfaces the account again or alerts anyone when the date passes. So accounts just sit there unless an agent manually goes looking for them." — Gareth Evans (Stakeholder interview)

**Source Dataset:** recovery_activity_tracker_sample.csv + delinquent_accounts_sample.csv

**Operational Observation:** 319 accounts carry a "Promise Due" status in the portfolio sample, with no system mechanism to enforce or escalate when those dates pass. The absence of automated triggering means promise commitments break silently — the account simply re-enters the Awaiting Follow-Up backlog with no flag distinguishing it from a new delinquency. This is the top-ranked unmet job in the JTBD analysis (JTBD-04).


#### PP-05: Poor Visibility for Managers

**Stakeholder Quote:**

"Reporting is meaningless because status codes mean different things to different teams, and activity logs fail to differentiate a successful call from a busy tone. Audit trails are scattered across email, standalone spreadsheets, and a 20-year-old database." — stakeholder_interview_notes.csv

**Source Dataset:** delinquent_accounts_sample.csv + stakeholder_interview_notes.csv

**Operational Observation:** 69 accounts in the portfolio sample carry no status at all — Missing or Unassigned. Beyond these edge cases, the broader problem is that the same status label may represent different operational states across teams, making portfolio-level reporting unreliable. Leadership cannot accurately forecast recovery yields or identify where the process is breaking without manual cross-referencing across three disconnected systems.


#### PP-06: No Vulnerability Flagging

**Stakeholder Quote:**

"Honestly, recognition is mostly down to experience and gut instinct. There's no flag in the system that says this is a vulnerable customer unless someone's manually added a note previously. Agents pick up on cues during the call — someone mentions illness, job loss, sounds distressed — or they spot patterns in the account history." — Gareth Evans (Stakeholder interview)

**Source Dataset:** stakeholder_interview_notes.csv

**Operational Observation:** The legacy system handles routine delinquencies and severe hardship cases identically. There are no distinct workflows, routing rules, or escalation triggers for vulnerable customers. Daniel Okoye confirmed this represents a real FCA regulatory risk — firms must identify and respond appropriately to customers showing signs of financial difficulty or vulnerability. The hardship escalation path is a manual email to a shared inbox with no formal handoff workflow and no confirmation mechanism.


#### PP-07: Shift Handover Information Loss

**Stakeholder Quote:**

"There's a handover process on paper, but in practice it's patchy. Agents are supposed to log notes in the collections database, but the database is clunky and slow, so people often leave quick notes in spreadsheets or emails instead. The next shift might not see those, or they see them too late." — Amina Rahman (Stakeholder interview)

**Source Dataset:** recovery_activity_tracker_sample.csv

**Operational Observation:** The activity tracker indicates approximately 20% of customer follow-ups are lost entirely at shift handovers. Because the legacy database is too slow to use reliably mid-shift, agents default to spreadsheet or email notes that exist outside the system of record. Incoming agents begin the next shift without visibility of what was agreed, promised, or attempted, forcing them to restart the duplicate check process from Step 1.


#### PP-08: Random Contact Ordering

**Stakeholder Quote:**

"It's less a deliberate policy and more that we never built the infrastructure to do it differently. The legacy system doesn't score accounts or prioritise queues — it just shows you a list, and agents work through it however makes sense to them. Some will sort by balance, some by days overdue, some just start at the top." — Amina Rahman (Stakeholder interview)

**Source Dataset:** delinquent_accounts_sample.csv

**Operational Observation:** The portfolio sample shows accounts distributed across a wide range of delinquency stages and risk profiles with no evidence of systematic contact ordering. High-value or high-risk accounts can sit untouched while agents work lower-priority cases. At 100,000+ accounts with a fixed team size, this is a direct recovery yield problem — the accounts most likely to respond to early intervention are not being prioritised for contact.


#### PP-09: Zero Cross-Channel Context

**Stakeholder Quote:**

"From scratch, unfortunately. If someone's been through the app or the phone menu first, we don't see any of that journey when they land with us. The call just comes through and we're starting fresh — asking them to verify details, explain what they're calling about, the lot." — Gareth Evans (Stakeholder interview)

**Source Dataset:** stakeholder_interview_notes.csv

**Operational Observation:** The collections system operates entirely separately from Legacy-Trust's main customer service platform. There is no shared view of interaction history across channels. When a customer is transferred to a collections agent after attempting self-service or contacting another team, all prior context is lost. The agent must re-establish the full situation from the beginning, wasting the opening minutes of every transferred call and requiring the customer to repeat their situation — including any vulnerable or distressing circumstances — from scratch.


### How the process currently feels

#### Customer

The current process is opaque, repetitive, and anxiety-inducing. A customer who falls into past-due status has no self-service option — they must call in to understand their balance or explore repayment options, even for the most straightforward enquiry. Because customers are not told that online payment options exist, they average 3 calls to resolve a single query, repeating their financial situation — and in some cases their personal hardship — across multiple transfers with no context carried between them. If the customer is vulnerable, their protection depends entirely on whether the agent they happen to speak to notices the signs during the call. There is no system support, no written confirmation of what was agreed, and no guarantee that a promise made on one shift will be remembered by the next agent who touches the account.


#### Collections Agent

The current process is exhausting, duplicated, and trust-eroding. Before an agent can make a single productive contact, they must complete a two-system check — Legacy DB for balance and status, then the Spreadsheet Tracker to confirm no colleague has already worked the account. The tracker is often out of date, so this check frequently fails to prevent duplicate outreach. Across the shift, an estimated 60–70% of agent time is absorbed by admin — re-keying status updates, reconciling spreadsheets, manually logging promises, and setting callback dates the system will never enforce. The queue offers no signal about which accounts are most urgent. Agents set follow-up reminders that only exist in their own memory. At the end of a shift, the database is too slow to update properly, so agents leave notes in emails or spreadsheets that the incoming team may never find. Skilled people are spending the majority of their working day on work a functional system would handle automatically.


#### Team Leader / Manager

The current process makes meaningful management almost impossible. There is no real-time visibility of which accounts are being worked, by whom, or at what stage. Status codes mean different things across teams, so reporting cannot be trusted. The manager cannot distinguish high-risk time-sensitive accounts from low-priority ones without manual investigation. If a callback is missed — which happens frequently — there is no automated alert. Accounts simply accumulate in the Awaiting Follow-Up backlog with no nudge to surface them. Shift handovers depend entirely on individual agent diligence, and when that fails under volume pressure, the manager only finds out when a customer calls back frustrated. A previous attempt to fix callback enforcement was raised with IT and deprioritised. New agents take two extra weeks to reach basic productivity because the tribal workarounds that hold the process together are never formally documented.

### 3. Self-Service Candidates

#### Self-Service Candidate Assessment

|Step / Activity                       |High Volume|Repeatable|Rules-Driven|Lower Risk|Verdict              |
|--------------------------------------|-----------|----------|------------|----------|---------------------|
|Customer checks account balance       |Yes        |Yes       |Yes         |Yes       |✅ Self-service      |
|Customer submits Promise to Pay       |Yes        |Yes       |Yes         |Yes       |✅ Self-service      |
|Customer requests Payment Plan setup  |Yes        |Yes       |Partial     |Partial   |⚠ Phase 1b           |
|Customer updates contact details      |Yes        |Yes       |Yes         |Yes       |✅ Self-service      |
|Automated follow-up reminder (PTP)    |Yes        |Yes       |Yes         |Yes       |✅ Self-service      |
|Status check / duplicate contact check|Yes        |Yes       |Yes         |Yes       |✅ Automate          |
|Callback date enforcement trigger     |Yes        |Yes       |Yes         |Yes       |✅ Automate          |
|Spreadsheet reconciliation            |Yes        |Yes       |Yes         |Yes       |✅ Eliminate via sync|
|Vulnerability identification          |Yes        |No        |No          |No        |❌ Agent-led only    |
|Hardship escalation routing           |Yes        |Partial   |Partial     |No        |❌ Agent-led only    |
|Complex payment negotiation           |Medium     |No        |No          |No        |❌ Agent-led only    |
|Dispute resolution                    |Medium     |No        |No          |No        |❌ Agent-led only    |

#### Automation Opportunity List


##### AO-01: Promise-to-Pay Self-Service Capture

**What it automates:** Customer submits a promise-to-pay commitment via portal — date and amount confirmed — without agent involvement.

**Pain point link:** PP-04 — Manual Promise-to-Pay Tracking

**JTBD link:** JTBD-04 — "When a customer requests a specific follow-up date, I want the system to strictly enforce that callback schedule, so that I never lose track of a hot lead or break a promise to a customer."

**Phase:** Phase 1 — confirmed primary anchor journey.

**Rationale:** Single date input, clear rules, no negotiation required, works across eligible and ineligible risk bands. Modelled conversion rate of 89.9% in planning scenarios.

##### AO-02: Automated Callback Triggering

**What it automates:** When a callback date passes, the system automatically surfaces the account in the agent queue with a flag — no manual checking required.

**Pain point link:** PP-02 — Missed and Delayed Follow-Up; PP-04 — Manual PTP Tracking

**JTBD link:** JTBD-04 — enforced callback scheduling; JTBD-03 — automated queue prioritisation at shift start.

**Phase:** Phase 1 — technically self-contained; does not require platform integration.

**Rationale:** Entirely rules-driven — if date = today and status = Promise Due then surface account. No judgement required.

##### AO-03: Real-Time Status Synchronisation

**What it automates:** Eliminates manual re-keying between Legacy DB and Spreadsheet Tracker by synchronising status updates automatically on every action.

**Pain point link:** PP-01 — Duplicate Status Checks; PP-03 — Spreadsheet Reconciliation Waste; PP-05 — Poor Manager Visibility

**JTBD link:** JTBD-05 — "When I log the outcome of a customer interaction, I want to select from standardised, mutually exclusive status codes, so that the history of the account is perfectly clear to anyone who inherits the case."

**Phase:** Pre-Phase 1 dependency — status standardisation must happen before portal rules can be built reliably.

**Rationale:** Pure data synchronisation — rules-based, high-volume, zero judgement required.

##### AO-04: Customer Balance and Account Summary View

**What it automates:** Customer can check their outstanding balance, days past due, and current account status via portal without calling in.

**Pain point link:** PP-09 — Zero Cross-Channel Context; PP-08 — Random Contact Ordering

**JTBD link:** JTBD-01 — "When I fall into past-due status, I want to have clear self-service control over my account balance and payment options, so that I can manage my financial obligations privately without the anxiety of a manual collections call."

**Phase:** Phase 1 — foundational customer-facing portal function.

**Rationale:** Read-only data display, no decision-making, no vulnerability risk, extremely high volume.

##### AO-05: Risk-Based Queue Prioritisation

**What it automates:** Agent queue automatically ordered by risk band, days past due, and recovery likelihood — agents always work the highest-priority accounts first.

**Pain point link:** PP-08 — Random Contact Ordering; PP-02 — Missed and Delayed Follow-Up

**JTBD link:** JTBD-03 — "When I log in to start my shift, I want to be automatically guided to the highest-priority customer accounts in a strategic sequence, so that I am maximising my recovery efforts rather than guessing who to call next."

**Phase:** Phase 2 — requires clean status foundation and queue management infrastructure.

**Rationale:** Entirely rules-driven — risk flag, DPD, and recovery likelihood are data fields that can be ranked without human judgement.

##### AO-06: Automated Follow-Up Reminder Notifications

**What it automates:** System automatically sends SMS or email reminder to customer when a promise date is approaching — reducing no-contact dropout before the promise date is reached.

**Pain point link:** PP-02 — Missed and Delayed Follow-Up; PP-04 — Manual PTP Tracking

**JTBD link:** JTBD-01 — customer self-service; JTBD-04 — enforced follow-up scheduling

**Phase:** Phase 1b — requires compliance sign-off on messaging templates before deployment.

**Rationale:** Templated, rules-driven, no personalisation beyond account data. Timing trigger is simple: if promise date = T-2 days then send reminder.

#### Steps That Must Remain Agent-Led

The following steps involve complexity, risk, or judgement that cannot be safely automated and must remain entirely agent-led, regardless of portal scope.

**Vulnerability identification**
There is no data signal that reliably identifies a vulnerable customer before a conversation begins. Recognition requires human judgement during the call — tone of voice, emotional distress, mentions of illness or job loss, or erratic payment patterns visible only in context. A portal cannot safely make this assessment. Gareth Evans confirmed this explicitly. FCA guidance requires firms to identify and respond appropriately — automated misclassification creates regulatory and welfare risk.

**Hardship escalation and specialist routing**
Once vulnerability is identified, the escalation path must be human-controlled. The specialist queue handoff requires full context, judgement about urgency, and confirmation the case has been received. An automated routing rule alone is insufficient — agent oversight of the handoff is required to meet FCA standards.

**Complex payment negotiation**
Customers in genuine financial difficulty may need arrangements that fall outside standard templates — partial payments, extended timelines, product restructuring. These require negotiation, empathy, and legal knowledge that cannot be encoded in portal rules without creating unfair outcomes.

**Dispute resolution**
Any case where the customer contests the balance, disputes a charge, or raises a complaint must be handled by an agent with access to the full account history and authority to investigate. Automated dispute handling creates legal and regulatory exposure.
