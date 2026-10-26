# Is the everyday Australian better off? (data to June quarter 2026)

Built by `src/auseconomy/households.py`; tables `living_costs`, `household_income`, `affordability`, `wealth_by_age`.

**Living costs vs CPI (Q2 2026 vs 2019 average).** Every household type except self-funded retirees has faced faster cost growth than headline CPI (+28.0%): employee households +31.2% (highest), other government transfer recipients +30.9%, pensioner and beneficiary +29.9%, age pensioners +29.0%, self-funded retirees +26.7%. The latest annual change is 3.7% for employees but 4.7% for age pensioners and 4.6% for other transfer recipients, so the gap has flipped towards benefit households recently.

**Real household income.** Real gross disposable income per capita (deflated by the household consumption deflator) was $15,313 per quarter in 2026-Q2, up 4.5% on 2019 but 5.3% below the 2021-Q3 stimulus peak ($16,173). The ABS measure, real net national disposable income per capita, is 5.6% above 2019 ($19,409 vs $18,385) and 4.1% below its 2022-Q2 peak ($20,246). The household saving ratio is 6.5%, versus 5.9% in 2019 and a 2020-21 spike. (June 2026 population is extrapolated; flagged by `pop_estimated`.) Averages mask distribution: income per head has recovered, but wages have not (WPI +22.2% since 2019 vs CPI +28.0%, about -4.5% real).

**Housing.** CPI rents relative to wages are 1.8% above their 2019 average (rents +24.4%, WPI +22.2%): rents have broadly tracked wages, unlike prices. Mean dwelling price to full-time ordinary earnings was 8.0 in Dec 2019 and is 10.2 now (price $687k to $1.10m). An indicative repayment on an 80% loan at cash rate + 2.5pp is 63% of one full-time earnings, up from 34% in 2019; this is a stylised single-earner proxy, not an observed burden.

**Wealth by age (SIH 2017-18 and 2019-20, Table 10.2).** Median net worth of 55-64 households was 6.2x that of 25-34 households in 2017-18 ($936k vs $151k) and 5.7x in 2019-20 ($1.00m vs $176k). Means: 4.2x and 4.3x. The 15-24 means swing wildly (high sampling error). Home ownership among 25-34s rose from 36.7% to 40.7%, but this predates the 2020-26 price surge.

**Gaps.** No survey after 2019-20 is published (2022-23 does not exist), so wealth-by-age cannot show the post-COVID price boom. "Under 35" uses the 25-34 band because the ABS tables lack household counts to combine bands. Survey values are nominal.
