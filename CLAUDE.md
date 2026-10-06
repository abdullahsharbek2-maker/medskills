# medskills

A collection of Claude Code skills for inpatient physicians and medical
trainees, covering clinical documentation, differential diagnosis support,
and coding/evidence lookup during day-to-day rounding work.

## Ground rules for every skill in this repo

- **Draft only, never final.** Every note, code suggestion, or differential
  these skills produce is a draft for the supervising/attending physician to
  review, correct, and sign. Never present output as a finalized medical
  record entry or a diagnosis.
- **Never fabricate clinical data.** Vitals, labs, imaging findings, exam
  findings, medication doses, and allergy status must come from what the
  user provides. If something critical is missing (e.g., allergy status,
  code status), call it out explicitly as missing rather than inferring or
  inventing a plausible value.
- **PHI handling.** This runs in a shared/cloud coding environment, not a
  covered clinical system. Skills should prompt users to de-identify input
  (e.g., "Patient A", relative dates) rather than paste real names, MRNs, or
  exact birthdates, and should avoid writing real identifiers into any file
  committed to this repo.
- **Can't-miss first.** Any differential or triage output must surface
  high-risk/can't-miss diagnoses even when low-probability, separate from a
  probability-ranked list.
- **Cite and flag uncertainty.** Coding and evidence-lookup skills must
  flag where current payer/guideline rules should be verified rather than
  billed or acted on directly from the skill's output.
