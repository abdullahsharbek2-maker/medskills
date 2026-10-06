---
name: progress-note
description: Draft a daily inpatient progress note (SOAP format) from a physician's rounding notes — overnight events, vitals/labs trends, and a problem-by-problem plan. Use for "progress note", "SOAP note", or "write up today's note for..." requests.
---

# Daily progress note (SOAP)

Convert rounding notes into a structured SOAP-format progress note,
organized by problem list so it's fast to scan on rounds.

## Before writing

Ask for or flag as missing:
- Current code status (if this is a multi-day admission, confirm it hasn't
  changed)
- Today's vitals (at minimum: most recent set)

## Output structure

```
PROGRESS NOTE — Hospital Day #__

Overnight Events: (brief; "none reported" if truly none)

Subjective: (patient-reported symptoms/complaints today)

Objective:
  Vitals: (today's, with trend if prior values given — e.g., "Tmax 38.9 -> 37.4")
  I/Os: (if provided)
  Pertinent exam findings:
  Labs: (new/changed values; trend direction)
  Imaging/Studies: (new results)

Assessment & Plan: (numbered by problem, most active/acute first)
  1. [Problem] — brief status (improving/stable/worsening) + plan
  2. [Problem] — ...
  #. Prophylaxis: (VTE, GI, lines/Foley need reassessed)
  #. Disposition: (anticipated next step, barriers to discharge)

Code Status:
```

## Style

- Carry forward stable chronic problems briefly rather than dropping them.
- Call out any new finding that changes the plan explicitly (don't bury it
  in a long list).
- If a problem has been unresolved >48h with no plan change, flag it so the
  team notices stalled workups.
- End with: "Draft for physician review — verify all values against the
  chart before signing."
