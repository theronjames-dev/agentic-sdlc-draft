# Exception Queue
> Agent-generated list of cases requiring human judgment.
> The primary venue for human coordination — not standups, not status meetings.
> Humans show up when the system surfaces something it cannot resolve.
> Everything else runs.

---

## Metadata

| Field | Value |
|-------|-------|
| **ID** | EQ-[DOMAIN]-[NUMBER] (e.g. EQ-ROBOTICS-001) |
| **Title** | Short descriptive name |
| **Scope** | Which Outcome Specs and Contracts this queue covers |
| **Owner** | Constraint + Contract Owners jointly |
| **Last Refreshed** | YYYY-MM-DD HH:MM |

---

## Open Exceptions

> Sorted by priority descending. Oldest unresolved items first within each priority.
> Agent-populated. Human-resolved.

### 🔴 Critical — Requires immediate judgment

| EQ ID | Type | Spec / Contract | Description | Raised | Assigned | SLA |
|-------|------|----------------|-------------|--------|----------|-----|
| EQ-[ID] | *[Type]* | *[Reference]* | *[What the agent cannot resolve]* | YYYY-MM-DD | *[Name]* | *[Hours]* |

---

### 🟡 Elevated — Requires judgment within 48 hours

| EQ ID | Type | Spec / Contract | Description | Raised | Assigned | SLA |
|-------|------|----------------|-------------|--------|----------|-----|
| EQ-[ID] | *[Type]* | *[Reference]* | *[What the agent cannot resolve]* | YYYY-MM-DD | *[Name]* | 48h |

---

### ⬜ Standard — Requires judgment within current cycle

| EQ ID | Type | Spec / Contract | Description | Raised | Assigned | SLA |
|-------|------|----------------|-------------|--------|----------|-----|
| EQ-[ID] | *[Type]* | *[Reference]* | *[What the agent cannot resolve]* | YYYY-MM-DD | *[Name]* | *[Cycle]* |

---

## Exception Types

> Reference for classifying exceptions consistently.

| Type | Description | Typical Owner |
|------|-------------|---------------|
| **Intent Parse Failure** | Agent could not determine what the spec requires | Spec Owner |
| **Boundary Misclassification** | Capability classified incorrectly — not in boundary map | Contract Owner |
| **Constraint Conflict** | Two constraints in the same spec or across specs contradict | Spec Owner |
| **Contract Ambiguity** | Contract terms are not specific enough to evaluate against | Contract Owner |
| **Template Render Failure** | Generated output does not match expected structure | Engineering |
| **Environment Failure** | Execution failed due to environment, not logic | Engineering |
| **Runtime Failure** | System executed but task did not complete as expected | Engineering |
| **Strategic Judgment** | Tradeoff between constraints requires business decision | Product + Leadership |
| **Scope Boundary** | Request is outside current capability — needs honest routing | Spec Owner |

---

## Resolution Log

> Closed exceptions with resolution documented.
> Resolution must include: decision made, rationale, and whether spec/contract was updated.

| EQ ID | Type | Spec / Contract | Resolution | Decision | Spec Updated | Closed | Resolved By |
|-------|------|----------------|------------|----------|-------------|--------|-------------|
| EQ-[ID] | *[Type]* | *[Reference]* | *[What was decided]* | *[Rationale]* | Yes / No | YYYY-MM-DD | *[Name]* |

---

## Exception Patterns

> Recurring exception types signal systemic issues — not one-off failures.
> Review monthly. If a type appears 3+ times, the underlying spec or contract needs revision.

| Type | Count (Last 30 Days) | Trend | Action Needed |
|------|---------------------|-------|---------------|
| *[Type]* | 0 | — | — |

---

## Queue Health

| Metric | Value | Target |
|--------|-------|--------|
| Open exceptions | 0 | < 5 |
| Avg resolution time (critical) | — | < 4 hours |
| Avg resolution time (elevated) | — | < 48 hours |
| Exceptions older than SLA | 0 | 0 |
| Recurring patterns unaddressed | 0 | 0 |
