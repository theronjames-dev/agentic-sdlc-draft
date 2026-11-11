# Confidence Dashboard
> Live view of how well the current codebase satisfies each committed Outcome Spec.
> No TPM research. No status meeting. No "let me check with the team."
> The dashboard is the status.

---

## Metadata

| Field | Value |
|-------|-------|
| **ID** | CD-[DOMAIN]-[NUMBER] (e.g. CD-ROBOTICS-001) |
| **Title** | Short descriptive name |
| **Scope** | Which Outcome Specs and Delivery Sequences this dashboard covers |
| **Owner** | System (agent-generated) |
| **Last Refreshed** | YYYY-MM-DD HH:MM |
| **Revision** | *[commit + dirty-file hashes the scores were computed on]* |
| **Environment** | *[Toolchain, runtime, and test environment versions]* |

---

## System Confidence Summary

> Top-line view. Updated on every evaluation run.

| Status | Count | % of Total |
|--------|-------|-----------|
| ✅ Passing (≥80%) | 0 | 0% |
| 🟡 At Risk (50–79%) | 0 | 0% |
| 🔴 Failing (<50%) | 0 | 0% |
| ⚪ Unavailable (check could not run) | 0 | 0% |
| ⏳ Stale (inputs changed since last run) | 0 | 0% |
| ⬜ Not Run | 0 | 0% |
| **Total Specs** | **0** | |

**Overall System Confidence:** `0%`

> Keep four things separate and never average them into one number: functional correctness, architecture (contract conformance), evidence validity, and the human outcome.
> A failed critical invariant shows as failing whatever the aggregate says. Unavailable and Stale are not passing.

---

## Outcome Spec Confidence

> Per-spec confidence scores. Sorted by confidence ascending (lowest first).
> Flat or declining scores for 2+ evaluation cycles trigger Exception Queue entry.

| Spec ID | Title | Confidence | Trend | Last Changed | Owner |
|---------|-------|------------|-------|-------------|-------|
| OS-[ID] | *[Title]* | `0%` | — | YYYY-MM-DD | *[Name]* |

---

## Delivery Sequence Status

> Aggregate confidence by delivery stage.

| Sequence ID | Partner | Stage | Stage Confidence | Overall |
|-------------|---------|-------|-----------------|---------|
| DS-[ID] | *[Partner]* | Stage 1 | `0%` | `0%` |

---

## Capability Contract Health

> Contracts with degraded support state or recent breaking changes.
> Healthy contracts not shown — only those requiring attention.

| Contract ID | Title | Support State | Dependent Specs | Issue |
|-------------|-------|--------------|----------------|-------|
| CC-[ID] | *[Title]* | Partial / Unsupported | *[n]* | *[Description]* |

---

## Prevention

> The metric that matters is how much the gate still finds. See [The Factory That Can't Fail](https://theronjames.substack.com/p/the-factory-that-cant-fail).

| Metric | Value | Target |
|--------|-------|--------|
| Late discoveries this cycle (found at the gate or after) | 0 | 0 |
| Late discoveries by cause | *[spec gap / contract gap / missing check / stale evidence / defect]* | — |
| Independent-check coverage (% of active specs with a check the builder didn't write) | 0% | — |

> Zero discoveries does not prove zero defects. Keep independent inspection running to challenge shared blind spots, and reward honest reporting.

---

## Check Enforcement

> Which protections actually run, and where. A check described only in instructions is advisory.

| Check | Protects | Status | Runs In |
|-------|----------|--------|---------|
| *[Check name]* | *[Spec / Contract]* | Planned / Advisory / Enforced | *[Pre-push hook, CI, merge gate, none]* |

---

## Confidence Trends

> Track trajectory over evaluation cycles.
> Flat confidence is as important a signal as declining confidence.

| Spec ID | Cycle -3 | Cycle -2 | Cycle -1 | Current | Trend |
|---------|---------|---------|---------|---------|-------|
| OS-[ID] | — | — | — | `0%` | — |

---

## Exception Queue Summary

> Open items requiring human judgment.
> Full detail in Exception Queue (EQ) artifact.

| EQ ID | Spec / Contract | Exception Type | Assigned To | Age |
|-------|----------------|---------------|-------------|-----|
| EQ-[ID] | *[Reference]* | *[Type]* | *[Name]* | *[Days]* |

---

## Evaluation Run Log

> Record of when evaluations were run and what changed.

| Run ID | Timestamp | Specs Evaluated | Changes Detected | Exceptions Raised |
|--------|-----------|----------------|-----------------|-------------------|
| — | YYYY-MM-DD HH:MM | 0 | 0 | 0 |

---

## Dashboard Notes

> Human-authored context that the confidence scores don't capture.
> Keep brief. If it belongs in an Exception Queue entry, put it there instead.

*[Any context worth noting]*
