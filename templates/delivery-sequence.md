# Delivery Sequence
> Business delivery order for a related set of Outcome Specs.
> Captures partner adoption path without creating spec-to-spec dependencies.
> The dependency graph stays clean — all relationships mediated through Capability Contracts.

---

## Metadata

| Field | Value |
|-------|-------|
| **ID** | DS-[DOMAIN]-[NUMBER] (e.g. DS-ROBOTICS-001) |
| **Title** | Short descriptive name |
| **Owner** | Product + Partner jointly |
| **Partner / Customer** | Who this delivery sequence is designed for |
| **Version** | 0.1 |
| **Status** | Draft / Active / Complete |
| **Created** | YYYY-MM-DD |
| **Target Completion** | YYYY-MM-DD |

---

## Adoption Narrative

> Two to four sentences. What is the partner trying to achieve?
> What does their journey look like from first contact to full capability?
> This is the "why this order" explanation — not a status report.

*[Write adoption narrative here]*

---

## Delivery Stages

> Ordered stages of value delivery for this partner.
> Each stage must be independently valuable — the partner gains something real at each step.
> Stages reference Outcome Specs, not individual features or tasks.

### Stage 1 — [Stage Name]

**Partner Value:** *[What the partner can do after this stage that they couldn't before]*

| Spec ID | Title | Confidence | Notes |
|---------|-------|------------|-------|
| OS-[ID] | *[Spec title]* | `0%` | |

---

### Stage 2 — [Stage Name]

**Partner Value:** *[What the partner can do after this stage that they couldn't before]*

| Spec ID | Title | Confidence | Notes |
|---------|-------|------------|-------|
| OS-[ID] | *[Spec title]* | `0%` | |

---

### Stage 3 — [Stage Name]

**Partner Value:** *[What the partner can do after this stage that they couldn't before]*

| Spec ID | Title | Confidence | Notes |
|---------|-------|------------|-------|
| OS-[ID] | *[Spec title]* | `0%` | |

---

## Sequence Confidence

> Aggregate view. Agent-generated when system is active.

| Stage | Specs | Avg Confidence | Stage Status |
|-------|-------|---------------|--------------|
| Stage 1 | *[n]* | `0%` | ⬜ Not started |
| Stage 2 | *[n]* | `0%` | ⬜ Not started |
| Stage 3 | *[n]* | `0%` | ⬜ Not started |

**Overall Sequence Confidence:** `0%`

---

## Blocking Dependencies

> Capability Contracts that are blocking sequence progress.
> Populated when a contract's support state prevents a spec from advancing.

| Contract ID | Blocking Stage | Issue | Owner | ETA |
|-------------|---------------|-------|-------|-----|
| — | — | — | — | — |

---

## Partner Success Criteria

> How you and the partner agree success is defined at sequence completion.
> These should mirror the Outcome Specs but expressed in business terms.

- *[Business outcome 1]*
- *[Business outcome 2]*
- *[Business outcome 3]*

---

## Revision History

| Version | Date | Author | Change |
|---------|------|--------|--------|
| 0.1 | YYYY-MM-DD | *[Name]* | Initial draft |
