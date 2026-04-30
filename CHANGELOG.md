# Changelog

All notable changes to the Pipeline Velocity Calculator.

## [1.2.0] - 2026-04-29

### Fixed

- Calculator content was getting cut off at the bottom when embedded in Webflow via iframe
- Revenue Intelligence Assessment results (especially when more than 2 reality check boxes appeared) were hidden below the iframe boundary

### Added

- Iframe detection script that communicates content height to parent frame via `postMessage` (`gtmlayer-calc-height` message type)
- MutationObserver to detect DOM changes and send updated height after results render
- Automatic overflow adjustment when running inside an iframe context

## [1.1.0] - 2026-04-29

### Added

- Revenue Intelligence Assessment -- 10-question diagnostic across Signal-Based Qualification and Signal-Driven Outbound
- Velocity Gap estimate showing current vs signal-driven potential with percentage uplift
- Category-level scoring (Qualification and Outbound scored independently, 0-100)
- Tier system: Manual and Reactive, Partially Instrumented, Signal-Aware, Signal-Driven
- Contextual insights generated based on category scores
- SEO and AEO optimisation: FAQ schema markup, SoftwareApplication schema, meta tags
- Updated hero copy and typography to match GTM Layer brand system (Inter Tight, JetBrains Mono)

## [1.0.0] - 2026-04-28

### Added

- Initial pipeline velocity calculator
- Core formula: (Opportunities x Win Rate x Deal Size) / Sales Cycle
- Period toggle: daily, weekly, monthly, quarterly views
- Pipeline breakdown: expected revenue, expected deals, pipeline coverage
- Lever analysis: models 10% improvement across each variable, identifies biggest lever
- What-if builder: simultaneous slider adjustment across all four levers with compound effect modelling
- Responsive design for desktop and mobile
- Deployed to GitHub Pages
