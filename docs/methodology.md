# Methodology

How each calculator in `index.html` works, and what it leaves out.

## Funnel scorecard (Step 1)

For each campaign, with spend in rupees:

```
qualified     = leads × qualification rate
accounts      = qualified × account-opening rate
activated     = accounts × first-trade rate

cost per lead       = spend ÷ leads
cost per qualified  = spend ÷ qualified
cost per account    = spend ÷ accounts
cost per activated  = spend ÷ activated
```

The page ranks campaigns twice, by cost per lead and by cost per activated customer, and shows how far each moves between the two rankings. The blended total uses the sums of all counts, not an average of the campaign rates.

**Limits.** It assumes the three rates are measured on the same cohort of leads. Leads that qualify or open accounts after your reporting window ends are undercounted, so use a date range that is long enough for the slowest stage.

## Signal picker (Step 2)

Chooses the deepest event (qualified lead, account opened or first trade) whose monthly volume is at or above the minimum you set. The enquiry itself is never chosen. The default minimum of 30 is a rule of thumb, not a platform requirement.

## Target translator and ROAS (Step 3)

```
goal target for an event = target cost per activated × (activated ÷ event count)
starting target          = today's cost per event × (1 + headroom)
target ROAS              = (yearly revenue × years counted) ÷ target cost per activated
payback (years)          = target cost per activated ÷ yearly revenue
```

The conversion rate from the event to activated is taken from the blended totals in the scorecard.

**Limits.** Revenue per customer is an input, not a forecast. It does not model churn, ramp-up of trading activity or the difference between segments. Agree the value and the number of years with Finance.

## Reallocation simulator (Step 4)

For each campaign, with a spend change of `Δ` and a return exponent `e` (between 0.5 and 1):

```
new spend      = spend × (1 + Δ)
new activated  = activated × (1 + Δ) ^ e
```

With `e = 1` every extra rupee converts as well as the average. With `e < 1`, extra spend converts worse and cuts lose less than proportionally. The "Same budget, shift to best" preset takes 30% from the two campaigns with the highest cost per activated customer and gives it equally to the two with the lowest. "Scale everything +40%" applies +40% to every campaign.

**Limits.** One exponent for every campaign is a simplification. Real response curves differ by campaign and flatten at different points. Use the simulator to compare ideas, then confirm with small real moves.

## DIY channel mix (Step 4)

```
blended cost   = DIY share × DIY cost + (1 − DIY share) × assisted cost
RM-handled     = monthly activations × (1 − DIY share)
RMs needed     = RM-handled ÷ activations per RM per month   (rounded up)
```

**Limits.** It assumes the cost per activation in each channel stays constant as the share changes, and that self-serve customers are as valuable as assisted ones. Check both with your own data.

## Everything the page stores

Only the checklist ticks, in the visitor's own browser (local storage). Nothing is sent anywhere.
