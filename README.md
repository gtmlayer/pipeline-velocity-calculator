# Pipeline Velocity Calculator & Revenue Intelligence Score

A free, open-source pipeline velocity calculator built for B2B SaaS revenue teams. Calculate your daily pipeline velocity, identify your biggest revenue lever, and benchmark your revenue intelligence against enterprise GTM teams.

**Live tool:** [gtmlayer.com/tools/pipeline-velocity-calculator](https://www.gtmlayer.com/tools/pipeline-velocity-calculator)

## What it does

Enter your pipeline numbers and the calculator gives you:

- **Pipeline velocity** -- how fast revenue moves through your pipeline, displayed as daily, weekly, monthly, or quarterly
- **Lever analysis** -- models a 10% improvement across each of the four levers (opportunities, win rate, deal size, sales cycle) and shows which one moves the needle most for your specific pipeline
- **What-if builder** -- adjust sliders across all four levers simultaneously to model compound scenarios
- **Revenue Intelligence Assessment** -- a 10-question diagnostic across Signal-Based Qualification and Signal-Driven Outbound that scores your GTM maturity and estimates the velocity gap between your current systems and signal-driven operation

## The formula

```
Pipeline Velocity = (Opportunities x Win Rate x Deal Size) / Sales Cycle (days)
```

The output is revenue per day. The calculator converts this to weekly, monthly, or quarterly views using simple multipliers (7, 30, 90).

## Revenue Intelligence Score

The diagnostic covers two categories, each scored 0-100:

- **Signal-Based Qualification** (5 questions) -- how you qualify deals, track engagement, prioritise pipeline, and progress stages
- **Signal-Driven Outbound** (5 questions) -- how you build lists, trigger sequences, personalise outreach, use intent data, and handle engagement

Total score maps to four tiers: Manual and Reactive (0-30), Partially Instrumented (31-55), Signal-Aware (56-80), Signal-Driven (81-100).

The velocity gap estimate uses a 0.35 multiplier against the intelligence gap, modelled from 6sense, Instantly, and Apollo 2026 benchmark data. See [METHODOLOGY.md](METHODOLOGY.md) for the full breakdown.

## Tech stack

- Vanilla HTML, CSS, and JavaScript
- No frameworks, no dependencies, no build step
- Single file (`index.html`) -- runs in any browser
- Inter Tight + JetBrains Mono from Google Fonts and Bunny Fonts
- Designed to be embedded via iframe with dynamic height resizing

## Embedding

The calculator includes built-in iframe detection. When embedded, it automatically communicates its content height to the parent frame via `postMessage`.

**Parent page listener:**

```html
<script>
window.addEventListener('message', function(e) {
  if (e.data && e.data.type === 'gtmlayer-calc-height' && e.data.height) {
    var iframe = document.querySelector('iframe');
    if (iframe && iframe.contentWindow === e.source) {
      iframe.style.height = e.data.height + 'px';
    }
  }
});
</script>
```

**Iframe embed:**

```html
<iframe
  src="https://gtmlayer.github.io/pipeline-velocity-calculator/"
  style="width: 100%; border: none; min-height: 800px;"
  title="Pipeline Velocity Calculator"
></iframe>
```

## Local development

No build step required. Just open `index.html` in a browser:

```bash
open index.html
```

Or serve it locally:

```bash
python3 -m http.server 8000
```

## Hosted on

- **GitHub Pages:** [gtmlayer.github.io/pipeline-velocity-calculator](https://gtmlayer.github.io/pipeline-velocity-calculator/)
- **Webflow (production):** [gtmlayer.com/tools/pipeline-velocity-calculator](https://www.gtmlayer.com/tools/pipeline-velocity-calculator)

## Related tools

- [Outbound Sequence Calculator](https://www.gtmlayer.com/tools/outbound-sequence-calculator) -- model deliverability, reply rates, and meetings booked for cold outbound campaigns

## Built by

[GTM Layer](https://www.gtmlayer.com) -- we build the intelligence layer between your tools and your revenue.

## Licence

MIT -- see [LICENSE](LICENSE) for details.
