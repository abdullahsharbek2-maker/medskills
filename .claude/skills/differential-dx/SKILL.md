---
name: differential-dx
description: Build a structured differential diagnosis from a clinical vignette, with can't-miss diagnoses separated from the probability-ranked list and suggested next workup steps. Use for "differential for...", "what could this be", or case-presentation questions from a physician or trainee.
---

# Differential diagnosis builder

This is decision-support for a licensed clinician who has the full
history, exam, and chart — not a diagnosis, and not a substitute for
clinical judgment or in-person evaluation. State this once, briefly, at
the top of the output, then get to the content.

## Process

1. Restate the key clinical features you're working from (age/sex, chief
   complaint, pertinent positives/negatives) in one line, so the user can
   immediately spot if you misread something.
2. If information critical to narrowing the differential is missing (e.g.,
   onset/timing, vitals, key exam findings), ask for it — don't guess and
   present a false level of confidence.
3. Build the differential in two explicit sections — never merge them:
   - **Can't-miss / high-risk diagnoses**: life- or limb-threatening
     possibilities that must be actively excluded regardless of how likely
     they are given the presentation.
   - **Probability-ranked differential**: most likely first, each with a
     one-line rationale tying it to the given features.
4. For each item in both lists, suggest the specific next step (history
   question, exam maneuver, lab, or imaging) that would most efficiently
   confirm or exclude it.
5. Close with what single piece of missing information would most change
   this differential, if applicable.

## Output structure

```
Working from: [one-line restatement of the case]

Can't-Miss Diagnoses:
  - [Diagnosis] — why it can't be missed — next step to exclude
  - ...

Differential (most to least likely):
  1. [Diagnosis] — rationale — next step to confirm/exclude
  2. ...

Most useful missing information: [if applicable]

This is decision support, not a diagnosis — correlate with full clinical
exam, local guidelines, and specialist input as needed.
```

## Style

- Don't pad the list with implausible diagnoses just to appear thorough —
  every entry needs a rationale tied to the actual case features.
- If the vignette is classic for one diagnosis, say so plainly rather than
  hedging across ten options.
