# Capability Contract
> A versioned declaration of what the system promises, and the boundary it is built inside.
> Agents read the applicable contract before choosing an implementation, not after.
> When this contract changes, every dependent Outcome Spec is immediately flagged.

---

## Metadata

| Field | Value |
|-------|-------|
| **ID** | CC-[DOMAIN]-[NUMBER] (e.g. CC-API-001) |
| **Title** | Short descriptive name |
| **Owner** | Engineering team or individual accountable for this capability |
| **Version** | 0.1 |
| **Status** | Draft / Active / Deprecated |
| **Created** | YYYY-MM-DD |
| **Last Updated** | YYYY-MM-DD |

---

## Capability Statement

> One or two sentences. What does this system component promise to deliver?
> Write from the consumer's perspective — what can they rely on?
> Must be specific enough that a breaking change is unambiguous.

*[Write capability statement here]*

---

## Boundary

> The engineering boundary this capability lives inside.
> Passing tests do not establish that these hold. Record them, then verify them.
> Prefer a few coherent contracts over one per class or file.

| Field | Entry |
|-------|-------|
| **Scope** | *[Subsystem and source locations covered]* |
| **Responsibility** | *[What it owns. Neighboring owners. What it explicitly does not own]* |
| **State and mutation** | *[Who owns mutable state, which operations may change it, what is read-only]* |
| **Lifetime** | *[Request / session / process. Behavior on reset, interruption, reload, and teardown]* |
| **Execution** | *[Where it runs in the scheduler or pipeline. When decisions become effects]* |
| **Dependencies** | *[Direction of dependencies. Lifetime of borrowed references, definitions, and assets]* |
| **Failure behavior** | *[Invalid input, unavailable resource, partial operation. What valid state is retained]* |

---

## Contract Terms

> The specific, versioned promises this contract makes.
> These are the terms dependent Outcome Specs rely on.
> Changing any term here triggers a flag on all dependent specs.

| ID | Term | Type | Value |
|----|------|------|-------|
| CT-01 | *[What is promised]* | Performance / Behavior / Interface / Availability | *[Specific value or definition]* |
| CT-02 | *[What is promised]* | Performance / Behavior / Interface / Availability | *[Specific value or definition]* |
| CT-03 | *[What is promised]* | Performance / Behavior / Interface / Availability | *[Specific value or definition]* |

---

## Known Failure Modes

> Explicit, honest documentation of where this capability breaks.
> Not aspirational — document current reality.
> This is what makes the contract trustworthy.

| ID | Failure Mode | Conditions | Retained State | Recommended Fallback |
|----|-------------|------------|----------------|----------------------|
| FM-01 | *[What breaks]* | *[When / under what conditions]* | *[What stays valid after the failure]* | *[What to use instead]* |
| FM-02 | *[What breaks]* | *[When / under what conditions]* | *[What stays valid]* | *[What to use instead]* |

> A required write that fails must surface as a failure. Never claim evidence exists when the write that produced it failed.

---

## Support State

> Current support level for this capability.

- [ ] **Supported** — Works reliably within documented terms. High confidence.
- [ ] **Partial** — Works in specific conditions. See known failure modes.
- [ ] **Unsupported** — Not currently viable. See recommended fallback.
- [ ] **Deprecated** — Being phased out. Migration path below.

**Confidence Level:** High / Medium / Low

**Notes:** *[Any additional context on support state]*

---

## Evidence and Conformance

> How you know the boundary and terms actually hold, on which revision.

| Check | Covers | Enforcement | Last Result | Revision |
|-------|--------|-------------|-------------|----------|
| *[Named check]* | *[Term or boundary field]* | Planned / Advisory / Enforced | Pass / Fail / Unavailable / Stale | *[commit]* |

**Conformance:** Established / Gap / Exception / Unverified

**Invalidated by:** *[Changes that make the evidence above stale: sources, data, contract version, tool or engine version, environment]*

> A check is **Enforced** only when the actual merge or status path runs it. Instructions alone are advisory.
> Promote a check to blocking only after it catches a planted violation and passes a valid control.

### Exceptions and Known Violations

> Existing violations are tracked debt, not passes. Writing a contract does not certify them. Do not worsen them.

| Invariant | Supported Conditions | Risk | Owner / Tracker | Expiry or Removal Trigger |
|-----------|---------------------|------|-----------------|---------------------------|
| *[What is violated]* | *[When it is safe]* | *[What could go wrong]* | *[Name / issue]* | *[Date or concrete trigger]* |

---

## Environment Requirements

> What must be true for this contract to hold.
> These are prerequisites, not aspirations.

```
- Requirement 1: [e.g. Pinned version X.Y.Z]
- Requirement 2: [e.g. Required asset set pre-installed]
- Requirement 3: [e.g. GPU driver >= version]
```

---

## Dependent Outcome Specs

> Outcome Specs that rely on this contract.
> Auto-populated by system when active. Manually tracked until then.

| Spec ID | Title | Impact if Contract Changes |
|---------|-------|---------------------------|
| OS-[ID] | *[Spec title]* | *[What breaks in that spec]* |

---

## Interface / API Reference

> Minimal reference for consumers of this capability.
> Link to full docs if they exist. Don't duplicate — just anchor.

```
[Interface definition, API signature, or reference link]
```

---

## Change Log

> Every change to contract terms must be logged here.
> Dependent Outcome Specs must be reviewed on any change.

| Version | Date | Author | Change | Specs Impacted |
|---------|------|--------|--------|----------------|
| 0.1 | YYYY-MM-DD | *[Name]* | Initial draft | — |

*Template revision 0.3 (2026-11-11): added Boundary, retained state on failure, and Evidence and Conformance with enforcement status and tracked exceptions.*
