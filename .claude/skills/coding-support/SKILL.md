---
name: coding-support
description: Suggest ICD-10-CM/CPT codes for an encounter and check whether the documentation supports the billed level of service (E/M), pointing out specificity gaps and missing MDM elements. Use for "what codes for this", "does this support a level 4/5 visit", or documentation-completeness questions.
---

# Coding & documentation support

Suggest codes and flag documentation gaps — final code selection and
compliance sign-off stays with the physician/coder. Always flag that
current payer- and CMS-specific rules should be verified before billing;
this is not a compliance determination.

## Process

1. From the note/encounter text provided, identify the diagnoses and
   services actually documented — do not infer a diagnosis or service that
   isn't stated.
2. Suggest ICD-10-CM code(s), preferring the most specific code the
   documentation actually supports (laterality, acute/chronic, episode of
   care, etc.). If the documentation only supports an unspecified code,
   say so and name what additional detail (e.g., "which side", "initial vs.
   subsequent encounter") would unlock a more specific one.
3. For E/M level questions, check documentation against the applicable
   framework (time-based, or Medical Decision Making: problems addressed,
   data reviewed, risk) and state plainly which level the documentation
   currently supports and what's missing to support a higher level —
   don't just assert a level without showing the gap.
4. For procedures, suggest CPT code(s) with a note on any missing element
   (e.g., modifier, documentation of approach/complexity) a biller would
   need.

## Output structure

```
Diagnoses documented -> Suggested ICD-10-CM:
  [finding as documented] -> [code] — [note if more specific code possible
  and what detail would get there]

Procedures documented -> Suggested CPT:
  [procedure] -> [code] — [note on modifiers/missing elements if any]

E/M Level Check (if applicable):
  Documentation currently supports: Level __
  To support Level __: [specific missing element]

Flags:
  - [anything documentation doesn't support but was billed/assumed]
  - [any unspecified code that could be more specific with more detail]

Verify against current CMS/payer-specific guidelines before billing — this
is coding support, not a compliance sign-off.
```

## Style

- Never suggest a code for something not actually in the documentation,
  even if it's clinically likely.
- Be concrete about the exact missing detail — "needs more documentation"
  is not useful; "needs laterality (left/right) to code beyond unspecified"
  is.
