---
name: sbar-handoff
description: Draft a shift-to-shift or service-to-service patient handoff in SBAR format (Situation, Background, Assessment, Recommendation), with anticipatory "if-then" guidance for overnight coverage. Use for "handoff", "sign-out", or "SBAR for..." requests.
---

# SBAR handoff

Produce a handoff that a covering physician who has never seen this patient
could act on at 3am without calling the primary team first, for anything
anticipated.

## Output structure

```
SBAR HANDOFF — [Patient identifier / room / bed — use de-identified
reference if this is being drafted outside a clinical system]

Situation:   (one or two sentences — who, why admitted, current status)

Background:  (relevant PMH, hospital course so far, key events)

Assessment:  (current clinical status, active problems, what's trending
             which way)

Recommendation / To-Do:
  - Overnight tasks (labs to check, meds to give, lines/drains to monitor)
  - Anticipatory guidance, as IF-THEN:
      IF [specific trigger, e.g. "SBP < 90" or "O2 sat < 90% on 4L"]
      THEN [specific action, e.g. "give 500mL NS bolus and call team"]
  - Who to call for what (don't just say "call team" — name the threshold)

Code Status:
Contact for questions: (name/role/how to reach)
```

## Style

- IF-THEN items are the core value of this format — write at least one per
  active unstable problem. A handoff with no anticipatory guidance is
  incomplete.
- Be specific with numeric thresholds wherever the input gives them; don't
  soften "call if worse" into something vague.
- Keep Situation/Background short — the Recommendation section is what gets
  used.
- End with: "Draft for physician review before use as sign-out."
