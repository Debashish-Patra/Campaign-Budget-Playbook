# Campaign Budget Playbook

An interactive guide to optimising a digital acquisition budget for **activated customers** (accounts opened and first trade placed) instead of cheap enquiries. It is built around a worked case from Indian broking (Franchise and Retail demat acquisition) and includes calculators you can edit with your own campaign numbers.

**Live page:** `https://<your-username>.github.io/<repo-name>/` (after you enable GitHub Pages, see below)

## The four steps

1. **Set the baseline.** Split performance by campaign, keyword, audience, lead source and segment. Capture cost per lead, qualification rate, account-opening rate, first-trade rate and cost per activated customer.
2. **Fix the conversion signals.** Connect the ad platforms to the CRM and to the account-opening and trading events, so bidding sees who qualified, opened and traded.
3. **Move bidding up in stages.** Target CPA on a reliable event first, then value-based bidding and target ROAS once conversion values are dependable.
4. **Reallocate towards quality.** Shift spend to the campaigns and segments that produce activated customers, and grow the self-serve (DIY) channel so growth does not depend on relationship-manager capacity.

The full text version is in [`docs/playbook.md`](docs/playbook.md).

## What is in this repository

```
index.html                       The interactive playbook (a single self-contained page)
docs/
  playbook.md                    Text version of the four steps, formulas and gates
  benchmarks.md                  Industry figures with sources, dates and calculations
  methodology.md                 How each calculator works, and its limits
templates/
  campaign-scorecard.csv         Step 1: baseline data template
  signal-mapping.csv             Step 2: conversion-event mapping template
  launch-checklist.md            The 12-item checklist as GitHub task boxes
CONTRIBUTING.md                  How to propose changes
CHANGELOG.md                     Version history
.nojekyll                        Tells GitHub Pages to serve the files as they are
```

## Run it locally

Open `index.html` in a browser. It has no build step and no dependencies other than the Google Fonts stylesheet, which falls back to system fonts when offline.

```
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Publish it with GitHub Pages

1. Push this folder to a GitHub repository.
2. Open the repository's **Settings**, then **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then select the `main` branch and the `/ (root)` folder, and save.
4. After a minute, the page is live at the address shown on that screen.

Pages on a private repository needs a paid GitHub plan. On a free plan, keep the repository public or share the folder another way.

## Adapt it to your own business

- **Campaign rows.** In `index.html`, find the array named `D` near the top of the script and replace the six example campaigns. The columns are spend (₹ lakh), leads, and the three funnel rates (percent).
- **Case study.** The Case section and the scoreboard beside it hold the original figures. Replace them with your own, or remove the section.
- **Benchmarks.** Update the Benchmarks table in `index.html` and `docs/benchmarks.md` together, and change the retrieval date in both. Steps are in `docs/benchmarks.md`.
- **Currency and units.** Amounts use Indian grouping (lakh and crore). Change the formatting helpers (`inr`, `num`, `spendFmt`) near the top of the script for other markets.

## Before you publish

- **Confidential figures.** The Case section includes budget, target and CAC figures from a real programme. Confirm you are allowed to share them. If the repository will be public, replace them with ranges or an anonymised example.
- **Benchmarks age quickly.** Check the retrieval date in the Benchmarks table and refresh the figures before you share the link.
- **Illustrative inputs.** The six example campaigns, relationship-manager capacity and the assisted and self-serve costs are placeholders, not data. Keep the label that says so.
- **Licence.** No licence file is included, which means all rights are reserved. Add one (for example MIT or CC BY 4.0) if you want others to reuse the content.

## Disclaimer

This is a planning aid and not financial, investment or legal advice. Calculator outputs depend entirely on the inputs you enter. Check current ad platform documentation for exact conversion-import methods and bid strategy requirements, and confirm data-sharing and consent practices with your compliance team.
