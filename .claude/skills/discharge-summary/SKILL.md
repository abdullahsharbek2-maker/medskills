---
name: discharge-summary
description: Draft a hospital discharge summary from the admission details and hospital course notes — diagnoses, course, medication reconciliation, pending results, and follow-up. Use for "discharge summary", "write up the discharge for...", or end-of-admission summary requests.
---

# Discharge summary

Produce a discharge summary that a receiving outpatient provider could act
on without needing the full chart. The two highest-risk sections —
medication reconciliation and pending results — get their own explicit
callouts, not just a mention in prose.

## Before writing

Ask for or flag as missing:
- Home medication list prior to admission (needed to reconcile against
  discharge meds)
- Any pending labs/cultures/imaging at time of discharge
- Follow-up appointments arranged

## Output structure

```
DISCHARGE SUMMARY

Admission Date:          Discharge Date:
Admitting Diagnosis:     Discharge Diagnosis(es):

Hospital Course:
  (chronological or by-problem narrative — what happened, key decision
  points, response to treatment, complications if any)

Procedures Performed:

Discharge Medications:
  NEW:        [med, dose, reason started]
  CHANGED:    [med, old dose -> new dose, reason]
  STOPPED:    [med, reason stopped]
  CONTINUED UNCHANGED: [med, dose]
  -> Flag explicitly if the home medication list was not fully reconciled.

Pending Results at Discharge:
  [test] — ordered [date], expected [when], who is responsible for
  follow-up on the result]
  -> If none, state "No pending results" explicitly rather than omitting
  this section.

Follow-up Appointments:
  [provider/specialty, timeframe, reason]

Discharge Condition / Functional Status:

Patient Instructions / Education Given:

Code Status at Discharge:
```

## Style

- Medication reconciliation errors are a leading cause of post-discharge
  harm — never collapse the NEW/CHANGED/STOPPED/CONTINUED categories into
  a single list.
- If the user didn't supply a home medication list, do not assume
  "continued unchanged" for anything — mark it unconfirmed.
- End with: "Draft for physician review — verify all medications, results,
  and follow-up details against the chart before signing."
