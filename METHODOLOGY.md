# Methodology

How the Pipeline Velocity Calculator and Revenue Intelligence Assessment work, what data they reference, and what the numbers mean.

## Pipeline Velocity Formula

The core formula is standard across revenue operations:

```
Pipeline Velocity = (Opportunities x Win Rate x Deal Size) / Sales Cycle
```

Where:

- **Opportunities** = number of active qualified opportunities in pipeline
- **Win Rate** = percentage of opportunities that close (entered as %, converted to decimal)
- **Deal Size** = average closed-won deal value
- **Sales Cycle** = average number of days from opportunity creation to close

The result is **revenue per day**. The calculator multiplies by 7, 30, or 90 for weekly, monthly, and quarterly views.

### Pipeline breakdown metrics

- **Expected Revenue** = Opportunities x Win Rate x Deal Size (total expected value from current pipeline)
- **Expected Deals** = Opportunities x Win Rate (number of deals expected to close)
- **Pipeline Coverage** = (Opportunities x Deal Size) / (Daily Velocity x 90) (how much pipeline you have relative to quarterly velocity target)

## Lever Analysis

The lever analysis models a 10% improvement to each variable independently, holding the others constant:

| Lever | Modelled change |
|---|---|
| More Opportunities | +10% to opportunity count |
| Higher Win Rate | +10% to win rate |
| Larger Deal Size | +10% to average deal size |
| Shorter Sales Cycle | -10% from average cycle length |

The calculator compares the resulting velocity for each scenario and identifies the **biggest lever** -- the single change that produces the largest velocity increase for your specific numbers.

This matters because the highest-impact lever is different for every team. A team with a 40% win rate and 200-day sales cycle gets more from shortening the cycle. A team with a 10% win rate and 30-day cycle gets more from improving conversion.

## What-If Builder

The what-if builder allows simultaneous adjustment of all four levers via sliders (-50% to +100%). This models compound effects, which is where the real gains live. Improving win rate by 15% while shortening your sales cycle by 20% compounds to more than the sum of each change alone.

## Revenue Intelligence Assessment

### Structure

The assessment has 10 questions across two categories:

**Signal-Based Qualification (Q1-Q5)**

| Question | What it measures |
|---|---|
| How do you qualify new opportunities? | Qualification methodology maturity |
| What signals inform your pipeline? | Data richness in deal evaluation |
| How do you track buyer engagement? | Engagement visibility |
| How do you prioritise pipeline? | Prioritisation sophistication |
| Stage progression is... | Automation and signal-driven progression |

**Signal-Driven Outbound (Q6-Q10)**

| Question | What it measures |
|---|---|
| How do you build prospect lists? | List sourcing maturity |
| What triggers your outbound sequences? | Trigger sophistication |
| How is outbound personalised? | Personalisation depth |
| Do you use intent data for prospecting? | Intent data integration |
| Reply and engagement handling is... | Response handling automation |

### Scoring

Each question has four options scored 0-3:

- **0** = No system or fully manual
- **1** = Basic or ad hoc
- **2** = Structured but not signal-driven
- **3** = Fully signal-driven or automated

Each category has a maximum raw score of 15 (5 questions x 3 points). Raw scores are normalised to 0-100.

**Total score** = average of both categories, normalised to 0-100.

### Tier mapping

| Score | Tier | What it means |
|---|---|---|
| 0-30 | Manual and Reactive | Pipeline runs on gut feel and manual processes |
| 31-55 | Partially Instrumented | Some systems in place but signals do not drive decisions |
| 56-80 | Signal-Aware | Signals inform parts of the pipeline but the full intelligence layer is not connected |
| 81-100 | Signal-Driven | Systems operate with real revenue intelligence |

### Velocity Gap Estimate

The velocity gap models how much additional pipeline velocity a team could unlock by moving to signal-driven operations.

```
Gap Percentage = (100 - Total Score) x 0.35
Potential Velocity = Current Velocity x (1 + Gap Percentage / 100)
```

The **0.35 multiplier** is a conservative modelled estimate based on compound lever effects from published benchmarks:

**Sources:**

- **6sense Business Impact Framework (2025-2026):** Customers report 2x deal sizes and 25% shorter sales cycles when intent data drives pipeline prioritisation
- **Instantly 2026 Cold Email Benchmark Report:** Signal-triggered outbound sequences convert at 3-5x the rate of cold list outbound
- **Apollo 2026 GTM Report:** Signal-targeted outbound achieves 2.37% cold-to-meeting rate versus 0.5-1.5% industry average
- **Winning by Design:** Enterprise SaaS benchmarks of 15-22% win rates and 90-180 day sales cycles

The 0.35 multiplier is deliberately conservative. It models a fraction of the theoretical maximum improvement, accounting for implementation friction, team adoption curves, and the diminishing returns as teams move from low to high maturity.

### Insight generation

The assessment generates contextual insights based on category scores:

- **Low qualification score (raw <= 7):** Highlights the qualification gap and references 25-35% conversion rate improvement from signal-based qualification
- **Mid qualification score (raw 8-11):** Focuses on the transition from checklist-based to signal-informed qualification and multi-threading data
- **Low outbound score (raw <= 7):** Highlights the conversion difference between cold list outbound (<1%) and signal-triggered outbound (1.2-3.2%)
- **Mid outbound score (raw 8-11):** Focuses on the timing gap between filtered lists and signal-triggered prospecting
- **Both low (qual <= 5, outbound <= 5):** Highlights the absence of an intelligence layer connecting systems
- **High total (>= 70):** Focuses on tightening feedback loops and expansion plays

## Limitations

- The velocity formula is a simplified model. Real pipeline dynamics include stage-specific conversion rates, deal aging, and pipeline decay
- The Revenue Intelligence Score is a self-assessment, not an audit. Scores depend on honest answers
- The velocity gap estimate is directional, not predictive. Actual results depend on implementation quality, team size, market conditions, and tech stack
- Benchmarks referenced are from 2025-2026 publications and may shift as the market evolves
- The 0.35 multiplier is a single coefficient across all maturity levels. In practice, low-maturity teams may see larger gains from foundational changes, while high-maturity teams see smaller marginal improvements
