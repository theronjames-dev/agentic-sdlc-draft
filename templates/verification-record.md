# Verification Record
> What was actually checked, on which revision, with what result.
> Written by the completion step, not by the agent's summary of its own work.
> Immutable once written. A rerun gets a new record.

---

## Identity

| Field | Value |
|-------|-------|
| **ID** | VR-[DOMAIN]-[NUMBER] |
| **Outcome Specs** | *[OS-IDs this record covers]* |
| **Capability Contracts** | *[CC-IDs and versions or content hashes]* |
| **Revision** | *[commit]* |
| **Dirty inputs** | *[Uncommitted files and their hashes, or "none"]* |
| **Environment** | *[OS, toolchain, runtime, engine, test environment versions]* |
| **Produced by** | *[Command or wrapper that wrote this record]* |
| **Date** | YYYY-MM-DD HH:MM |

---

## Checks

> Valid results: Pass, Fail, Unavailable, Stale. A successful process exit alone does not establish the intended effect.
> A missing tool is Unavailable, never a pass inherited from an older run.

| Check | Covers | Command | Result | Evidence Path | Notes |
|-------|--------|---------|--------|---------------|-------|
| *[Name]* | *[AC-ID / CT-ID]* | `[command]` | Pass / Fail / Unavailable / Stale | *[log, capture, report]* | |

---

## Skipped and Unavailable

| Check | Reason | Claims Left Unresolved |
|-------|--------|------------------------|
| *[Name]* | *[Why it did not run]* | *[What cannot be claimed as a result]* |

---

## Invalidation

> Changes that make this record stale for the claims above. Revalidate only what is affected: a spelling fix in documentation does not invalidate unrelated test results.

- *[Source paths, data files, contract versions, tool versions, environment changes]*

---

## Remaining Gaps

> Known failures, open contract exceptions, and anything this record does not establish. Human acceptance is never established here.

- *[Gap]*
