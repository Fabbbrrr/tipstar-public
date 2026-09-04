# tipstar · public

Public read-only mirror of the **tipstar** dashboard and static reports. This
repo exists so the site can live on **GitHub Pages for free** (Pages requires a
public repo — the full source stays private in the `tipstar` repo).

## What's here

A small navigatable site — every page has the same top nav bar linking to all
the others:

| Page | What it is |
|---|---|
| [`index.html`](https://fabbbrrr.github.io/tipstar-public/) | The live dashboard: current tips, settled results, headline stats, drift gate, and a 14-day walk-forward backtest. |
| [`review.html`](https://fabbbrrr.github.io/tipstar-public/review.html) | **Model vs market** — a fresh prequential (no-lookahead) backtest on the most recent settled date, with the full research grounding and sources. |
| [`model.html`](https://fabbbrrr.github.io/tipstar-public/model.html) | How the model works: conditional-logit scoring, feature list, selection rules, and the walk-forward audit. |
| [`data.html`](https://fabbbrrr.github.io/tipstar-public/data.html) | The data contract: the exact schema the pipeline expects from a bookmaker feed. |
| [`gaps.html`](https://fabbbrrr.github.io/tipstar-public/gaps.html) | What this repo deliberately does **not** do, and the open limitations. |

## How it updates

This repo is **not edited by hand.** The private `tipstar` project runs a nightly
scheduled job that:

1. settles yesterday's tips against the actual results,
2. rebuilds the whole site (dashboard + review + docs pages),
3. pushes every page here.

GitHub Pages then redeploys automatically. So the site stays current on its
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
