# Everwell Care Dashboard (Prototype)

Interactive prototype of **Everwell 2.0**, a hardware-agnostic B2B SaaS dashboard that helps home-care coordinators decide **whom to visit first**, based on sustained changes in older adults' wearable data (steps, sleep, resting heart rate, HRV) measured against each person's own baseline.

> Care-visit prioritisation tool — not a diagnostic device. All data is simulated.

## Live demo
Open `index.html` in a browser, or visit the GitHub Pages site for this repo.

## What it shows
- **Today's priorities**: 12 simulated clients sorted High → Watch → Data gap → Stable
- **Client detail**: plain-language "why flagged" note, 7/30-day trend charts with a shaded personal "usual range" band
- **Visit workflow**: schedule a wellness visit and record its outcome; the list updates instantly
- **How it works**: data flow, detection method, GDPR notes

## Detection approach (simulated)
- 28-day personal baseline per metric
- z-scores for day-level deviations, EWMA for sustained drift, change-point detection for abrupt shifts
- An LLM only phrases already-computed flags; a human always decides

## Tech
Single static page: HTML, CSS, vanilla JS, Chart.js (bundled). State is kept in memory and resets on reload.

## Status
MVP prototype with mock data only. No real patient data is collected or stored.
