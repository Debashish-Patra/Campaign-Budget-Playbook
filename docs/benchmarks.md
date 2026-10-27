# Benchmarks

Figures retrieved on **27 October 2026**. Use them to sanity-check your own numbers, not to replace them.

**Type** column: *Reported* is a published figure. *Derived* is calculated here from published figures. *Secondary* is a blog or aggregator that does not name its own source.

## Market size and activity

| Measure | Figure | Period | Type | Source |
| --- | --- | --- | --- | --- |
| Demat accounts, India | 237.7 million; 3.3 million added in the month (2.9 million in July, over 2.5 million in June) | Aug 2026 | Reported | [Business Today](https://www.businesstoday.in/personal-finance/story/demat-accounts-are-growing-faster-than-active-investors-what-does-it-mean-for-brokerages-554079-2026-09-09), [Asianet](https://newsable.asianetnews.com/business/demat-account-additions-surge-in-july-2026-reach-234-4-million-articleshow-hykhvbp), [Sahi](https://www.sahi.com/news/nse-unique-client-codes-hit-26-crore-as-june-demat-additions-bounce-to-2-5-million-3932-PE1_COR) |
| FY26 gross demat additions | NSDL 59.3 lakh plus CDSL about 2.72 crore, about 3.3 crore combined | FY26 | Derived | [Outlook Money](https://www.outlookmoney.com/invest/nsdl-adds-59-lakh-demat-accounts-in-fy26-records-highest-ever-annual-expansion) |
| NSE active clients | About 46 million (Aug 2026); 4.57 crore at end FY26, down about 7% from 4.92 crore | Aug 2026, FY26 | Reported | [Angel One news](https://oga-prod.angelone.in/news/market-updates/nse-active-clients-down-7-in-fy26-accounts-falls-to-4-57-crore), [Business Today](https://www.businesstoday.in/personal-finance/story/demat-accounts-are-growing-faster-than-active-investors-what-does-it-mean-for-brokerages-554079-2026-09-09) |
| Active clients as a share of demat accounts | 19.3% industry; Angel One NSE activation 17% | Aug 2026 | Reported | [Business Today](https://www.businesstoday.in/personal-finance/story/demat-accounts-are-growing-faster-than-active-investors-what-does-it-mean-for-brokerages-554079-2026-09-09) |
| Share of NSE active clients | Groww 28.31%, Zerodha 15.08%, Angel One 14.79%; Motilal Oswal a marginal decline, no figure in the source | FY26 | Reported | [Angel One news](https://oga-prod.angelone.in/news/market-updates/nse-active-clients-down-7-in-fy26-accounts-falls-to-4-57-crore) |

## Acquisition and economics

| Measure | Figure | Period | Type | Source |
| --- | --- | --- | --- | --- |
| Angel One gross client additions | 1.80 million in the quarter, then about 1.5 million | Q4 FY26, Q2 FY27 | Reported | [Arihant Capital](https://www.arihantcapital.com/company-information/companynewsdetails/25107010049), [Yahoo Finance](https://finance.yahoo.com/markets/stocks/articles/angel-one-ltd-bom-543235-030042177.html) |
| Groww customer acquisition cost | ₹796 (H1 FY25), ₹1,374 (H1 FY26), ₹900 (Q3 FY26). The unit is not defined in the articles. | FY25 to FY26 | Reported | [Storyboard18, H1](https://www.storyboard18.com/brand-marketing/groww-q2-profit-hits-rs-471-crore-as-customer-acquisition-cost-nearly-doubles-to-rs-1374-84569.htm), [Storyboard18, Q3](https://www.storyboard18.com/brand-marketing/groww-cuts-branding-spend-in-q3-fy26-as-customer-acquisition-costs-fall-33-87630.htm) |
| Angel One revenue per NSE-active client | About ₹8,600 a year | Q4 FY26 | Derived | See calculation below |
| Angel One direct vs assisted channel | Net broking income split roughly 75 : 25 | Q2 FY27 | Reported | [Yahoo Finance](https://finance.yahoo.com/markets/stocks/articles/angel-one-ltd-bom-543235-030042177.html) |

## Funnel and search ads

| Measure | Figure | Period | Type | Source |
| --- | --- | --- | --- | --- |
| Sign-up to KYC completion | About 60% to 70% at leading Indian trading apps | Not dated | Secondary | [Fintech onboarding blog](https://www.piyushwadhwa.com/writing/fintech-onboarding-kyc-dropoff) |
| KYC completers who never trade | About 20% to 30% | Not dated | Secondary | [Fintech onboarding blog](https://www.piyushwadhwa.com/writing/fintech-onboarding-kyc-dropoff) |
| Search ads, finance and insurance | Median cost per click $3.39, conversion rate 2.64%, cost per lead $74.44 | Apr 2025 to Mar 2026 | Reported | [WordStream](https://www.wordstream.com/blog/2026-google-ads-benchmarks) |

The search ads figures cover 13,474 US campaigns and are in US dollars. Use them for ratios only.

## Derived calculations

**FY26 gross demat additions.** 59.3 lakh (NSDL) + 2.72 crore (CDSL) = about 3.31 crore.

**Where a target sits.** 1.5 lakh ÷ 3.31 crore = about 0.45%. 4.3 lakh ÷ 3.31 crore = about 1.3%.

**Angel One revenue per NSE-active client.**

1. NSE-active clients ≈ 14.79% × 4.57 crore ≈ 6.76 million.
2. Q4 FY26 revenue from operations ₹1,459.42 Cr, annualised (× 4) ≈ ₹5,838 Cr.
3. ₹5,838 Cr ÷ 6.76 million ≈ ₹8,640 a year, shown as about ₹8,600.

Caveats: one quarter annualised, all revenue lines included, a discount-led client base, and no adjustment for clients who traded on other days of the year.

## How comparable are these?

Digital-first brokers report ₹900 to ₹1,400 per customer. A franchise and relationship-manager model reporting ₹12K to ₹16K per *activated* customer counts a different thing (a customer who opened and traded, and likely a wider cost scope) under a different model. Compare trends and ratios, not the rupee figures.

## How to refresh

1. Check the latest monthly depository data (CDSL and NSDL) and the NSE active-client figure.
2. Check the latest quarterly results of the brokers you benchmark against for client additions, revenue and any disclosed acquisition cost.
3. Recalculate the derived rows above with the new inputs.
4. Update the table in `index.html`, this file, and the retrieval date in both.
5. Add a line to `CHANGELOG.md`.
