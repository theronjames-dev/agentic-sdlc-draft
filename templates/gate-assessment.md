# Gate Assessment
> An independent verdict on a judgment constraint, recorded before the human judge reviews.
> The context that built the work does not grade it.
> Predictions are compared against the human's judgment afterward. That comparison is how evaluation gets better.

---

## Identity

| Field | Value |
|-------|-------|
| **ID** | GA-[DOMAIN]-[NUMBER] |
| **Outcome Spec** | *[OS-ID and the judgment constraints under review]* |
| **Revision** | *[commit or build]* |
| **Evaluator** | *[Model or person, and confirmation it did not build this work]* |
| **Evaluator was given** | *[Gate brief, prior calibration entries, evidence. Not the diff or build history]* |
| **Date** | YYYY-MM-DD |

---

## Access

> What the evaluator actually observed. An unavailable channel is an evidence gap, not a passed check.

| Channel | Available | Notes |
|---------|-----------|-------|
| Logs / measurements | Yes / No | |
| Images / captures | Yes / No | |
| Video / audio | Yes / No | |
| Interactive use | Yes / No | *[Separate tool latency from system latency]* |

---

## Verdict

> Pass, Revise, or Inconclusive per layer. Explain mixed verdicts; never average them.
> Pass means the evidence meets the criteria. It is not human acceptance.

| Layer | Verdict | Evidence | Missing Evidence |
|-------|---------|----------|------------------|
| Mechanical correctness | | | |
| Perceptual / qualitative | | | |
| Outcome effectiveness | | | |

**Overall:** Pass / Revise / Inconclusive

> For a **Tune** spec, report each constraint as Holds / Not yet / Cannot tell, and name the value you would change and in which direction. There is no overall pass.

---

## Predictions (sealed)

> Store in a separate file the human opens after their own review. Specific and tied to scenarios. Include the strongest expected success and the most plausible weakness.

| ID | Prediction | Scenario | Basis |
|----|-----------|----------|-------|
| P-01 | *[What the judge will notice or decide]* | *[Where]* | *[Why]* |

---

## Calibration (after human review)

> Keep hits and misses. The human is authoritative about their own judgment; their judgment does not automatically identify the implementation cause.

| Prediction | Human Observation | Match / Mismatch / Not tested | Cause of Mismatch | Change to Evaluation |
|-----------|-------------------|-------------------------------|-------------------|----------------------|
| P-01 | | | Observation gap / Interpretation / Preference / Defect / Changed conditions | |

**Decision:** *[Human's acceptance or requested revision. Leave pending until given]*
