---
name: evidence-lookup
description: Answer a focused clinical question with a quick evidence/guideline summary during rounds — bottom line, supporting evidence with sources, and caveats. Use for "is there evidence for...", "what do guidelines say about...", or rounds-style clinical questions needing a sourced answer.
---

# Evidence & guideline lookup

Give a rounds-speed answer to a focused clinical question, sourced to real
guidelines/literature rather than general knowledge, and explicit about
where evidence is thin or guidelines disagree.

## Process

1. Restate the clinical question precisely, including the patient
   population if given (age, comorbidities) — evidence that doesn't match
   the population isn't useful.
2. Search for current guidelines (e.g., major society guidelines) and, if
   relevant, primary literature or recent meta-analyses, using WebSearch /
   WebFetch if available. Prefer guideline bodies and systematic
   reviews/meta-analyses over single studies unless the question specifically
   calls for a landmark trial.
3. If guidelines from different bodies disagree, say so explicitly rather
   than picking one silently.
4. Note the strength/quality of evidence behind the bottom line (e.g.,
   strong RCT evidence vs. expert consensus/observational only).

## Output structure

```
Question: [restated, with population if applicable]

Bottom Line: [direct answer in 1-2 sentences]

Evidence:
  - [Guideline/study] ([year]) — [finding relevant to the question]
  - ...
  (cite source names/organizations; link if fetched from the web)

Where guidelines disagree (if applicable):
  [body A] recommends X; [body B] recommends Y — [key difference in
  population/evidence driving the disagreement]

Caveats:
  - [population mismatch, evidence quality, applicability limits]

Not a substitute for institutional protocol or pharmacy/specialist
consultation for dosing or patient-specific decisions.
```

## Style

- If no good-quality evidence exists, say that plainly instead of
  presenting weak/anecdotal evidence as settled.
- Keep the Bottom Line answerable at a glance — the Evidence section is
  for whoever wants to verify it.
