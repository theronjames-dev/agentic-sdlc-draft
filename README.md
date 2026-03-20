# Post-Agentic SDLC Templates

**Five artifacts replace the entire current stack.**

Not five more documents. Five machine-readable structures that agents operate against continuously.

---

## The Problem

Every software methodology we have — waterfall, Agile, SAFe — was invented to solve the same problem.

*Code is expensive. How do we make sure we write the right code?*

User stories. Sprints. Story points. Acceptance criteria. PRDs. All of it is an answer to that one constraint.

AI just made that constraint obsolete.

When agent teams can generate, test, and iterate on code continuously, the bottleneck shifts. The question stops being *did we build the thing* and becomes *does the thing satisfy what we committed to.*

User stories cannot answer that question. They were never designed to.

---

## The Five Artifacts

| # | Artifact | Replaces | Owner |
|---|----------|----------|-------|
| 01 | [Outcome Spec](templates/outcome-spec.md) | User story + PRD | Product + Partner |
| 02 | [Capability Contract](templates/capability-contract.md) | SRD + implicit dependency web | Engineering |
| 03 | [Delivery Sequence](templates/delivery-sequence.md) | Roadmap + release plan | Product + Partner |
| 04 | [Confidence Dashboard](templates/confidence-dashboard.md) | Status meetings + TPM tracking | System |
| 05 | [Exception Queue](templates/exception-queue.md) | Standups + Slack coordination | Constraint + Contract Owners |

---

## The Non-Negotiable

Acceptance criteria must be executable. If a criterion cannot be run as a test, it is not a constraint — it is an opinion.

This is what separates the new model from better documentation. Outcome Specs are constraints that agents evaluate autonomously. The moment prose acceptance criteria enter the system, you've rebuilt the old model with a new name.

---

## How the Artifacts Relate

```
Outcome Spec
  └── depends on → Capability Contract(s)
                       └── when changed → flags dependent Outcome Specs

Delivery Sequence
  └── orders → Outcome Specs (by partner adoption stage)
  └── no direct spec-to-spec dependencies — all mediated through Contracts

Confidence Dashboard
  └── evaluates → all active Outcome Specs
  └── surfaces → Exception Queue entries

Exception Queue
  └── receives → cases agents cannot resolve
  └── resolved by → Constraint + Contract Owners
  └── closes loop → back to Outcome Spec or Capability Contract update
```

---

## Where to Start

Take one active user story. Rewrite the acceptance criteria so every single one is executable as a test.

Not *"the user can complete onboarding."* That is an opinion.

*"A new user with no prior account completes onboarding in under 4 minutes with zero support interactions."* That is a constraint.

If you cannot make an acceptance criterion executable, you do not yet know what you are building. That is useful information.

---

## Templates

- [Outcome Spec](templates/outcome-spec.md)
- [Capability Contract](templates/capability-contract.md)
- [Delivery Sequence](templates/delivery-sequence.md)
- [Confidence Dashboard](templates/confidence-dashboard.md)
- [Exception Queue](templates/exception-queue.md)

---

## Examples

*Coming soon — worked examples from a real prototype.*

---

## Background

These templates accompany the Substack post: **[The User Story Is Dead](https://theronjames.substack.com)**

---

## License

MIT. Use freely. Adapt to your context. If you build something interesting on top of this, share it.

---

*Built by [Theron James](https://theronjames.substack.com)*
