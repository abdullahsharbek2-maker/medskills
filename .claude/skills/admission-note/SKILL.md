---
name: admission-note
description: Draft a hospital admission History & Physical (H&P) from a physician's rough notes, dictation, or bullet points about a newly admitted patient. Use when the user says things like "write up this admission", "H&P for...", or pastes rough notes on a new inpatient.
---

# Admission note (H&P)

Turn a physician's rough notes/dictation into a structured, well-organized
H&P draft. Never invent data: only use what the user provides, and
explicitly flag anything safety-critical that's missing.

## Before writing

If any of these are missing from the input, ask for them (or mark the
section "NOT PROVIDED — confirm with team") instead of guessing:
- Allergies (including "NKDA" if truly none)
- Code status
- Home medications

## Output structure

```
ADMISSION NOTE / HISTORY & PHYSICAL

Chief Complaint:
HPI: (narrative, chronological, includes pertinent positives/negatives)
PMH:
PSH:
Family History:
Social History: (tobacco/alcohol/substance use, living situation, occupation)
Allergies:
Home Medications:
ROS: (by system, only systems reviewed)
Physical Exam: (vitals first, then by system — only findings given)
Labs / Imaging: (as provided; note if pending)
Assessment:
  One-line summary (age/sex, relevant PMH, presenting with X, likely Y)
Plan: (organized by problem/system, numbered)
  1. [Problem] — plan
  2. [Problem] — plan
Code Status:
Disposition / anticipated length of stay:
```

## Style

- Use standard medical abbreviations consistently; expand on first use if
  ambiguous.
- Keep the Assessment one-liner tight — this is what gets read on rounds.
- Plan items should be actionable (orders, consults, monitoring parameters),
  not just restated diagnoses.
- End with a one-line reminder: "Draft for physician review — verify all
  values against the chart before signing."
