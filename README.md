# tipstar · public

Public read-only mirror of the **tipstar** dashboard and static reports. This
repo exists so the site can live on **GitHub Pages for free** (Pages requires a
public repo — the full source stays private in the `tipstar` repo).

## What's here

| Path | What it is |
|---|---|
| `index.html` | The live dashboard: current tips, settled results, headline stats, drift gate, and a 14-day walk-forward backtest. |

More static reports will be dropped here as they're generated.

## How it updates

This repo is **not edited by hand.** The private `tipstar` project runs a nightly
scheduled job that:

1. settles yesterday's tips against the actual results,
2. regenerates the dashboard HTML,
3. copies it to `index.html` here and pushes.

GitHub Pages then redeploys automatically. So this page stays current on its
own — no manual steps.

## About tipstar

tipstar is a research greyhound-racing value model. It scores each race's
runners with a conditional-logit model trained on a book's own odds and
form, picks the best value picks, and settles them against the actual result
each night to track real performance and detect model drift.

- **Fixed-ROI** is the honest per-race number (bet at the posted price).
- **Tote-ROI** is the same bet settled at the official tote dividend.

Performance is reported as-is, including the losses. The model is built to sit
**at market** on fixed odds, with the research edge appearing (if anywhere)
on the tote. See the private `tipstar` repo for the full method, cites, and
limitations.

## Data sources

Odds, form, and results come from public bookmaker racing feeds (Sportsbet and
Ladbrokes Australia). No login or API keys are used; the feeds are public.

---
*Static site — no build step, no server, no secrets. Updated automatically.*
