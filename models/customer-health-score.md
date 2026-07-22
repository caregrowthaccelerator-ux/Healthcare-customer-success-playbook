# Customer Health Score Model

## Purpose

Create a transparent, explainable score that supports judgment rather than replacing it.

## Suggested dimensions

| Dimension | Weight | Example evidence |
|---|---:|---|
| Adoption | 30% | Active users, repeat use, workflow completion |
| Outcomes | 25% | Progress toward defined success metrics |
| Relationship | 20% | Sponsor engagement, champion strength, stakeholder coverage |
| Support and delivery | 15% | Issue severity, response patterns, implementation status |
| Commercial | 10% | Renewal timing, scope fit, payment or contracting risk |

## Scoring

Score each dimension from 1 to 5:

- **5 — Strong:** Consistently positive evidence
- **4 — Healthy:** Minor gaps with low risk
- **3 — Watch:** Mixed evidence or emerging risk
- **2 — At risk:** Significant gaps requiring a recovery plan
- **1 — Critical:** Immediate executive attention required

### Formula

`Health Score = Σ (dimension score ÷ 5 × dimension weight)`

The result is a percentage from 20% to 100%.

## Suggested bands

- **80–100%:** Healthy
- **65–79%:** Watch
- **Below 65%:** At risk

## Guardrails

- Document the evidence behind every score.
- Do not hide a severe risk inside an average.
- Add a manual “critical override” for safety, security, compliance, or executive-loss events.
- Review trends over time, not only the current number.
- Pair the score with a written next action.

## Example

| Dimension | Score | Weight | Weighted result |
|---|---:|---:|---:|
| Adoption | 4 | 30% | 24% |
| Outcomes | 3 | 25% | 15% |
| Relationship | 4 | 20% | 16% |
| Support and delivery | 3 | 15% | 9% |
| Commercial | 5 | 10% | 10% |
| **Total** |  |  | **74% — Watch** |
