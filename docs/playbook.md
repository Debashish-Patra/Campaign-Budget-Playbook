# The playbook in text

This is the plain-text version of the four steps in the interactive page. Use it for review, comments and version history.

## The problem

Cost per lead is the easiest number to improve and the easiest to be fooled by. A campaign that brings in enquiries cheaply can still be the most expensive way to get a customer who opens an account and trades.

Decide what a good outcome is, give the ad platforms that outcome as a signal, and move money towards what produces it.

| Optimising for | Instead of |
| --- | --- |
| Cost per qualified lead, then cost per activated customer | Lowest cost per lead |
| Share of leads that open an account and place a first trade | Highest enquiry volume |
| Conversion value and ROAS, once the data is dependable | Clicks, form fills, click-through rate |

## The worked case

- **Situation.** Digital acquisition for Franchise and Retail ran on a ₹50 Cr budget, with about ₹30 Cr in paid media across Google Search, Display and Demand Gen, and Meta. The FY25-26 target was about 1.5 lakh new demat accounts, a share of the company's 4.3 lakh.
- **What went wrong.** Spend was scaled by about 40%. Lead quality fell and acquisition cost rose.
- **Diagnosis.** The programme was optimising for cheap enquiries, not for customers who opened accounts and traded.
- **Result.** Blended CAC fell from about ₹16K to ₹12K (about 25%) while spend kept scaling, measured on activated customers rather than enquiries.

## Step 1. Set the baseline

Split performance by **campaign, keyword, audience, lead source and customer segment**. For each slice, record:

| Measure | Formula |
| --- | --- |
| Cost per lead (CPL) | spend ÷ leads |
| Qualification rate | qualified leads ÷ leads |
| Account-opening rate | accounts opened ÷ qualified leads |
| First-trade rate | first trades ÷ accounts opened |
| Cost per activated customer | spend ÷ first trades |

**Done when** every campaign has all five numbers from the same date range, and someone outside marketing agrees the account-opened and first-trade counts match the back office.

Template: [`templates/campaign-scorecard.csv`](../templates/campaign-scorecard.csv)

## Step 2. Fix the conversion signals

Connect Google Ads (and Meta) to the CRM and to the account-opening and trading events.

1. Capture the click ID when the lead arrives and store it on the lead record in the CRM.
2. When the lead status changes in the CRM, back office or trading platform, send that event back to the ad platform against the same click.
3. Report each event under its own name, so you can see cost per qualified lead as well as cost per activated customer.

| Signal | Where it lives | Speed | Role in bidding |
| --- | --- | --- | --- |
| Lead submitted | Website or lead form | Instant | Reporting only |
| Qualified lead | CRM status | Hours to days | First bidding target |
| Account opened | Onboarding or KYC system | Days | Intermediate target when trades are too few |
| First trade (activated) | Trading platform | Days to weeks | Best target, carries a value for ROAS bidding |

**Choosing the event.** Pick the deepest event that clears your minimum monthly conversions per campaign (the page defaults to 30, a rule of thumb, not a platform rule). If none does, pool similar campaigns or lengthen the window.

**Done when** a test lead can be followed from ad click to first trade, and the same event shows up in the ad platform under its own name within the expected delay.

Send only consented, hashed customer identifiers, and confirm the setup with your data-protection and compliance teams.

Template: [`templates/signal-mapping.csv`](../templates/signal-mapping.csv)

## Step 3. Move bidding up in stages

| Stage | Bidding | Move on when |
| --- | --- | --- |
| A | Clean data, no bid change | Platform and CRM counts agree within your tolerance |
| B | Target CPA on qualified lead | Enough qualified-lead conversions per campaign |
| C | Target CPA on activated customer | Cost per activated customer is stable week to week |
| D | Value-based bidding and target ROAS | Conversion values are dependable and approved by Finance |

**Translating a goal into a bid target.** Goal target for an event = target cost per activated customer × the share of that event's conversions that become activated. Start at today's cost for that event plus some headroom, then tighten in steps.

**Target ROAS** = revenue value counted per activated customer ÷ target cost per activated customer. **Payback** = target cost ÷ yearly revenue per activated customer.

**Done when** the campaign hits its target on the deepest event with enough volume, for several weeks in a row, before you move up a stage.

## Step 4. Reallocate towards quality

- Move budget in steps, then wait for results before the next move.
- Expect diminishing returns: extra spend on one campaign usually converts worse than the average.
- Judge every move on cost per activated customer.
- In parallel, grow the self-serve (DIY) channel so growth does not depend on relationship-manager capacity. The case moved DIY from about 7% towards 25% of volume.

**Done when** the reallocated mix beats the old one on cost per activated customer, and the DIY share is rising without lowering the quality of accounts opened.

## Checklist

See [`templates/launch-checklist.md`](../templates/launch-checklist.md).
