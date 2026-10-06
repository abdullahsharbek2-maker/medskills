# medskills

Claude Code skills for hospital-based physicians and medical trainees,
covering clinical documentation, differential diagnosis support, and
coding/evidence lookup for day-to-day rounding work.

All output is a **draft for physician review** — these skills never
fabricate clinical data and never present output as a final, signed record
or an actual diagnosis. See `CLAUDE.md` for the full ground rules shared
across every skill, including PHI-handling guidance for this environment.

## Skills

| Skill | Use for |
|---|---|
| `admission-note` | Drafting a History & Physical (H&P) for a new admission from rough notes/dictation |
| `progress-note` | Daily inpatient SOAP progress note from rounding notes |
| `discharge-summary` | End-of-admission discharge summary, with medication reconciliation and pending-results tracking |
| `sbar-handoff` | Shift-to-shift / service-to-service sign-out in SBAR format with anticipatory IF-THEN guidance |
| `differential-dx` | Structured differential diagnosis from a clinical vignette, with can't-miss diagnoses separated out |
| `coding-support` | ICD-10-CM/CPT code suggestions and E/M documentation-completeness checks |
| `evidence-lookup` | Sourced, rounds-speed answers to focused clinical questions against current guidelines/literature |

Each skill lives in `.claude/skills/<name>/SKILL.md` and is invoked as
`/<name>` in Claude Code, or triggers automatically when a request matches
its description.
