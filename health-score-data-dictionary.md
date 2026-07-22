# Customer Health-Score Data Dictionary

The definitions behind the health-score model — so the score is transparent, defensible, and reproducible instead of a black box. This makes the model easy to explain in an interview or to a skeptical stakeholder.

## Scoring model overview

Health score = weighted sum of category scores, normalized to 0–100 and bucketed into a status. Every input is defined below with its source, how it's measured, and why it matters.

## Status bands

| Band | Score | Meaning | Default action |
|------|:-----:|---------|----------------|
| Healthy | 80–100 | Adopting well, seeing value | Nurture, look for expansion |
| Watch | 60–79 | Some risk signals | Proactive check-in |
| At risk | 40–59 | Multiple warning signs | Intervention plan |
| Critical | 0–39 | Churn likely | Escalate immediately |

## Categories & weights

| Category | Weight | What it captures |
|----------|:------:|------------------|
| Product adoption | 30% | Are they actually using it? |
| Outcomes / value | 25% | Are they getting the result they came for? |
| Engagement | 20% | Are they responsive and involved? |
| Relationship | 15% | Champion strength and stakeholder breadth |
| Support / sentiment | 10% | Friction, complaints, tone |

## Field definitions

### Product adoption (30%)
| Field | Definition | Source | Signal |
|-------|-----------|--------|--------|
| Active usage rate | % of eligible tasks run through the workflow | Usage data | Low = adoption stalling |
| Feature depth | Using core steps incl. approval, not just surface | Usage data | Shallow = fragile |
| Trend | Usage rising, flat, or falling over 30 days | Usage data | Falling = leading churn signal |

### Outcomes / value (25%)
| Field | Definition | Source | Signal |
|-------|-----------|--------|--------|
| Goal progress | Movement toward the outcome set at onboarding | Success plan | Stalled = value at risk |
| Baseline vs. now | Metric improvement vs. pre-launch baseline | KPI tracking | Flat = ROI unproven |

### Engagement (20%)
| Field | Definition | Source | Signal |
|-------|-----------|--------|--------|
| Responsiveness | Replies to outreach within a reasonable window | CRM / email | Going quiet = risk |
| Meeting attendance | Shows up to check-ins / QBRs | Calendar | No-shows = disengagement |

### Relationship (15%)
| Field | Definition | Source | Signal |
|-------|-----------|--------|--------|
| Champion strength | Is there an active internal advocate? | CS judgment | No champion = fragile |
| Stakeholder breadth | Multiple contacts vs. single-threaded | Stakeholder map | Single point = high risk |

### Support / sentiment (10%)
| Field | Definition | Source | Signal |
|-------|-----------|--------|--------|
| Open issues | Unresolved friction or complaints | Support log | Piling up = frustration |
| Sentiment | Tone in interactions | CS judgment | Negative = escalate |

## Guardrails on the model

- **A critical signal overrides the average.** A single-threaded account with a departing champion is "at risk" even if usage looks fine.
- **Judgment fields are documented, not guessed.** Note *why* a relationship score is what it is.
- **Recalibrate quarterly.** Weights should reflect what actually predicted churn or expansion.
- **The score starts a conversation; it doesn't end one.** It tells you where to look, not what to conclude.
