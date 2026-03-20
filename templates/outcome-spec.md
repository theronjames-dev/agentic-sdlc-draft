# Outcome Spec
> Machine-evaluable constraints defining what a commitment requires.
> The spec and the test suite are the same artifact.

---

## Metadata

| Field | Value |
|-------|-------|
| **ID** | OS-[DOMAIN]-[NUMBER] (e.g. OS-DEV-001) |
| **Title** | Short descriptive name |
| **Owner** | Person accountable for defining "correct" |
| **Partner / Stakeholder** | Who this commitment is made to |
| **Version** | 0.1 |
| **Status** | Draft / Active / Deprecated |
| **Created** | YYYY-MM-DD |
| **Last Updated** | YYYY-MM-DD |

---

## Outcome Statement

> One or two sentences. What does success look like for the person this commitment is made to?
> Write from their perspective, not the system's perspective.
> Must be falsifiable — if you can't imagine what failure looks like, rewrite it.

*[Write outcome statement here]*

---

## Acceptance Constraints

> Every constraint must be executable as a test.
> If it cannot be run as a test, it is not a constraint — it is an opinion.
> Use specific numbers, thresholds, and observable behaviors.
> No prose like "the user should be able to..." — that is an opinion.

| ID | Constraint | Test Method |
|----|-----------|-------------|
| AC-01 | *[Specific, measurable, testable statement]* | *[How this is verified — automated test, benchmark, observation]* |
| AC-02 | *[Specific, measurable, testable statement]* | *[How this is verified]* |
| AC-03 | *[Specific, measurable, testable statement]* | *[How this is verified]* |

---

## What This Is Not

> Explicitly state what is out of scope.
> This prevents scope creep and keeps the spec honest.

- Not: *[excluded scope item]*
- Not: *[excluded scope item]*
- Not: *[excluded scope item]*

---

## Capability Contract Dependencies

> List the Capability Contracts this spec depends on.
> If a contract changes, this spec must be re-evaluated.

| Contract ID | Description | Impact if Changed |
|-------------|-------------|-------------------|
| CC-[ID] | *[What this contract covers]* | *[What breaks in this spec]* |

---

## Confidence Score

> Agent-generated. Do not manually edit once system is active.
> Represents current % of acceptance constraints passing.

**Current:** `0%` — Not started

| AC | Status | Last Run | Notes |
|----|--------|----------|-------|
| AC-01 | ⬜ Not run | — | |
| AC-02 | ⬜ Not run | — | |
| AC-03 | ⬜ Not run | — | |

---

## Strategic Connection

> Why does this spec exist?
> Connect to the strategic bet or platform objective it serves.
> If you can't answer this, the spec may not be worth writing.

*[Strategic bet or objective this serves]*

---

## What Stays Human

> List the judgment calls agents cannot make for this spec.
> These are the exception triggers that surface to the Exception Queue.

- *[Judgment call 1]*
- *[Judgment call 2]*

---

## Exception Log

> Agent-populated. Cases where human judgment was required.

| Date | Exception | Resolution | Owner |
|------|-----------|------------|-------|
| — | — | — | — |

---

## Revision History

| Version | Date | Author | Change |
|---------|------|--------|--------|
| 0.1 | YYYY-MM-DD | *[Name]* | Initial draft |
