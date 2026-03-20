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

---

## System Confidence Summary

> Top-line view. Updated on every evaluation run.

| Status | Count | % of Total |
|--------|-------|-----------|
| ✅ Passing (≥80%) | 0 | 0% |
| 🟡 At Risk (50–79%) | 0 | 0% |
| 🔴 Failing (<50%) | 0 | 0% |
| ⬜ Not Run | 0 | 0% |
| **Total Specs** | **0** | |

**Overall System Confidence:** `0%`

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
