# Outcome Spec
> Verifiable constraints defining what a commitment requires.
> The spec and its verification are the same artifact.

---

## Metadata

| Field | Value |
|-------|-------|
| **ID** | OS-[DOMAIN]-[NUMBER] (e.g. OS-DEV-001) |
| **Title** | Short descriptive name |
| **Owner** | Person accountable for defining "correct" |
| **Partner / Stakeholder** | Who this commitment is made to |
| **Mode** | Discovery / Delivery / Tune (see below) |
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

## Mode

> Name the mode. It decides what "done" means for this spec.

- **Discovery** — the outcome is not known yet. This spec is a claim to test, not a commitment to build. It closes on a decision (keep, change, cut), not on a merge. Fill in *Discovery Terms* below.
- **Delivery** — the outcome is chosen. Constraints define acceptance; agents build until they pass.
- **Tune** — the design is settled and the systems exist. Constraints are tuning acceptance. An unmet constraint means a value is wrong, not that the design is. Propose a structural change only when no value in the available range satisfies it, and record the range tried.

Do not silently turn a Discovery spec into a Delivery commitment, or treat a settled design as a hypothesis.

---

## Discovery Terms

> Discovery mode only. Write all of this before the run, not after.

| Field | Entry |
|-------|-------|
| **Claim** | *[What you believe, stated so it can be wrong]* |
| **Decision it informs** | *[What you will decide from the result]* |
| **Exposure condition** | *[What must actually occur for a run to count. If it never occurs, the run is void, not failed]* |
| **Confirming signal** | *[Observation + sample + threshold]* |
| **Contradicting signal** | *[Observation + sample + threshold. Rarely the arithmetic inverse of the confirming signal]* |
| **Listed confounds** | *[What would invalidate a run. Anything unlisted is inconclusive and costs a run]* |
| **Run cap** | *[Default 2 per question, then resolve or discard as unanswerable at this fidelity]* |

---

## Acceptance Constraints

> Every constraint names how it is verified.
> Mechanical constraints run as tests. Judgment constraints name the judge, the evidence, and a prediction recorded before the judge reviews.
> If a constraint has no named verification, it is not a constraint — it is an opinion.
> Use specific numbers, thresholds, and observable behaviors wherever the outcome allows. Do not invent a number for an experiential judgment.

> **Anti-patterns that make constraints un-executable:**
> - Intent language: "capable of," "should be able to," "importable" — these are opinions, not constraints
> - Implicit preconditions: "given the system is running" — name the exact system state, named data, and config
> - Missing error paths: what happens at the boundary is as important as the happy path
> - Scope bleed: if there is no "What This Is Not" section, the constraint is not done
> - Self-grading: the agent that built the work cannot be the judge of a judgment constraint

| ID | Constraint | Precondition | Verified By | Test Method / Judge | Boundary / Edge Case |
|----|-----------|--------------|-------------|---------------------|----------------------|
| AC-01 | *[Specific, measurable, testable statement]* | *[Exact system state required before this constraint applies]* | Test / Measurement / Judgment | *[Automated test or benchmark; for Judgment, who judges and from what evidence]* | *[What happens at the limit, on error, or when input is invalid]* |
| AC-02 | *[Specific, measurable, testable statement]* | *[Exact system state]* | Test / Measurement / Judgment | *[How this is verified]* | *[Edge case or error path]* |
| AC-03 | *[Specific, measurable, testable statement]* | *[Exact system state]* | Test / Measurement / Judgment | *[How this is verified]* | *[Edge case or error path]* |

---

## What This Is Not

> Explicitly state what is out of scope.
> This prevents scope creep and keeps the spec honest.
> The absence of this section is a signal the spec hasn't been scoped.
> Reference related spec IDs where applicable.

- Not: *[excluded scope item — reference OS-ID if covered elsewhere]*
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
> Represents current % of acceptance constraints passing **on the named revision**.
> Valid states: Pass, Fail, Unavailable, Stale, Not run. Only Pass counts toward the score.
> Unavailable verification is never a pass inherited from an earlier run. A change to a relevant source, contract, data, or environment makes affected results Stale until rerun.
> A failed critical constraint is reported as failing regardless of the percentage.

**Current:** `0%` — Not started · **Revision:** *[commit + dirty-file hashes]* · **Record:** *[link to Verification Record]*

| AC | Status | Revision | Last Run | Evidence | Notes |
|----|--------|----------|----------|----------|-------|
| AC-01 | ⬜ Not run | — | — | — | |
| AC-02 | ⬜ Not run | — | — | — | |
| AC-03 | ⬜ Not run | — | — | — | |

---

## Strategic Connection

> Why does this spec exist?
> Connect to the strategic bet or platform objective it serves.
> If you can't answer this, the spec may not be worth writing.

*[Strategic bet or objective this serves]*

---

## What Stays Human

> List the decisions agents cannot make for this spec: acceptance, taste, and tradeoffs between constraints.
> For each, name who decides and what evidence they decide from.
> An agent can still record its own verdict and predictions first (see [Gate Assessment](gate-assessment.md)). That is not acceptance.

| Decision | Who Decides | Evidence |
|----------|-------------|----------|
| *[Judgment call 1]* | *[Name]* | *[Sessions, measurements, captures]* |
| *[Judgment call 2]* | *[Name]* | *[Evidence]* |

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
| 0.2 | 2026-03-26 | Theron James | Added Precondition and Boundary columns to AC table; added anti-patterns note; strengthened What This Is Not guidance |
| 0.3 | 2026-11-11 | Theron James | Added Mode and Discovery Terms; constraints name their verification (test, measurement, or judgment with a named judge); confidence bound to a revision with Unavailable and Stale states; What Stays Human names who decides |
