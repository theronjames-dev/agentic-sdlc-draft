# Changelog

## 0.3 — 2026-11-11

Revisions from running the templates on real work, including the [Indie Game Outcomes](https://github.com/theronjames-dev/indie-game-outcomes) game-development application.

- **Non-Negotiable restated.** Every criterion names its verification. Mechanical criteria run as tests; judgment criteria name the judge, the evidence, and an independently recorded prediction. Unverified prose is still not a constraint.
- **Modes.** Outcome Specs declare Discovery, Delivery, or Tune. Discovery specs carry claim, decision, exposure condition, confirming and contradicting signals, listed confounds, and a run cap.
- **Capability Contract.** Added a Boundary section (responsibility, state and mutation, lifetime, execution, dependencies, failure behavior), retained state per failure mode, and Evidence and Conformance with enforcement status and tracked exceptions.
- **Confidence is revision-bound.** Results carry the revision they ran on. Unavailable and Stale are explicit states that never count as passing. Critical failures are not averaged away.
- **Confidence Dashboard.** Added Prevention (late discoveries by cause, independent-check coverage) and Check Enforcement (Planned / Advisory / Enforced).
- **Exception Queue.** Added Spec Gap, Contract Violation, Stale Evidence, Unavailable Verification, and Calibration Miss. Patterns are fixed with checks and detection tests, not more documentation.
- **New supporting records:** Verification Record, Gate Assessment, Harness Regression Set.

## 0.2 — 2026-03-26

Outcome Spec: added Precondition and Boundary columns, anti-patterns note, stronger What This Is Not guidance.

## 0.1 — 2026-03

Initial five artifacts: Outcome Spec, Capability Contract, Delivery Sequence, Confidence Dashboard, Exception Queue.
