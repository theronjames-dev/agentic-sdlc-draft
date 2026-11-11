# Harness Regression Set
> Evaluates how work gets produced: agent instructions, tools, model configuration, and completion rules.
> Product tests still evaluate the product.
> Use when changing the harness, or when the same kind of escape keeps happening.

---

## Metadata

| Field | Value |
|-------|-------|
| **ID** | HR-[DOMAIN]-[NUMBER] |
| **Harness version under test** | *[Instructions, tools, model, completion wrapper versions]* |
| **Baseline version** | *[What you are comparing against]* |
| **Fixture revision** | *[commit of the disposable fixture repo]* |
| **Date** | YYYY-MM-DD |

---

## Tasks

> A few tasks drawn from real failure classes. Run in disposable copies with no live trackers, publishing, or messaging side effects.
> Define success from requirements before running. Grade final artifacts and actual effects, not the agent's confidence or phrasing.

| Task | Failure Class It Targets | Observable Success | Grader |
|------|-------------------------|--------------------|--------|
| *[Extend a capability]* | *[Responsibility added to the wrong owner]* | *[Uses the declared owner and seam]* | Deterministic / Reviewer |
| *[Repair a failing test]* | *[Assertion weakened to manufacture a pass]* | *[Behavior fixed; assertions unchanged]* | Deterministic |
| *[Resume interrupted work]* | *[Unrelated changes overwritten]* | *[Inspects the actual tree; preserves unrelated work]* | Reviewer |
| *[Handle unavailable verification]* | *[Unavailable reported as pass]* | *[Reports Unavailable; leaves dependent claims unresolved]* | Deterministic |

---

## Grader Calibration

> Before a check blocks anything, show that it discriminates.

| Check | Valid Control Passes | Planted Violation Caught | Status |
|-------|---------------------|-------------------------|--------|
| *[Check]* | Yes / No | Yes / No | Advisory / Ready to enforce |

---

## Trials

> One successful run is a smoke result, not a reliability estimate. Report counts, conditions, failures, and cost. Keep misses.

| Task | Version | Trials | Passed | Failures Observed | Cost |
|------|---------|--------|--------|-------------------|------|
| *[Task]* | Baseline / Candidate | *[n]* | *[n]* | *[What went wrong]* | *[Time / tokens]* |

---

## Decision

> Adopt, revise, or drop the harness change. Narrow or remove process that blocks legitimate work or costs more than the feedback it gives.

*[Decision and rationale]*
