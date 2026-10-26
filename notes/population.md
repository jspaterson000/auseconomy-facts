# Population, immigration and ageing

**Data.** ABS API: `ERP_COMP_Q` (components, 1981Q2–2026Q1), `ERP_Q` (single-year age), and `POP_PROJ` (2022-based, Series B and zero NOM). Visa groups come from ABS *Overseas Migration 2024-25* cube 4. The latest ABS figure is **NOM of 292,100 in the year to March 2026** (released 17 Sep 2026). FY 2025-26 so far covers three quarters: 244,200.

## NOM forecast vs actual ('000)

| Vintage | 22-23 | 23-24 | 24-25 | 25-26 | 26-27 | 27-28 | 28-29 | 29-30 |
|---|---|---|---|---|---|---|---|---|
| Oct-22 Budget | 235 | 235 | 235 | 235 | | | | |
| May-23 Budget | 400 | 315 | 260 | 260 | 260 | | | |
| Dec-23 MYEFO | 510ᵉ | 375 | 250 | 255 | 235 | | | |
| May-24 Budget | 528ᵉ | 395 | 260 | 255 | 235 | 235 | | |
| Dec-24 MYEFO | | 446ᵉ | 340 | 255 | 225 | 225 | | |
| Mar-25 Budget | | 435ᵉ | 335 | 260 | 225 | 225 | 225 | |
| Dec-25 MYEFO | | | 310ᵉ | 260 | 225 | | | |
| May-26 Budget | | | 305ᵉ | 295 | 245 | 225 | 225 | 225 |
| **ABS actual** | **538** | **429** | **302** | 244 (3 qtrs) | | | | |

ᵉ = estimate for a year that had already ended. Sources: BP1 Table 2.2 and footnotes, BP3 Table A.5, MYEFO Table 2.2/2.3. URLs are in `NOM_SOURCES`. No 2022-23 MYEFO was published.

Treasury under-forecast NOM by 303k (2022-23, Oct-22 Budget) and by 114k (2023-24, May-23 Budget). It then over-forecast 2024-25 by 34–39k. The May-26 Budget's 295k for 2025-26 needs about 51k in the June quarter.

## Ageing: an age-adjusted standstill

Weights are per-person health, aged care and pension spending (2025-26: $128bn, $41bn, $67bn). For 0-14 / 15-64 / 65-74 / 75-84 / 85+ they are **0.25 / 0.41 / 2.45 / 4.35 / 9.04**. In the whole-budget variant, where other spending is age-neutral, they are 0.78 / 0.83 / 1.42 / 1.97 / 3.34.

⚠ **The age profiles are an approximation.** No official by-age table was found. Override them with `ageing(weights=...)`.

| Avg annual growth | Pop | Age-cost pop | Premium | Whole budget |
|---|---|---|---|---|
| 1999-00→2009-10 | 1.48% | 2.20% | +0.72pp | 1.66% |
| 2009-10→2019-20 | 1.53% | 2.50% | +0.97pp | 1.79% |
| 2019-20→2024-25 | 1.48% | 2.64% | +1.16pp | 1.81% |
| 2024-25→2029-30 | 1.35% | 2.73% | +1.39pp | 1.76% |

With the brief's weights (0.6/0.8/2/3.5/6), the 2024-25 to 2029-30 premium is +0.79pp. The old-age dependency ratio rises from 20.1 (2010) to 26.9 (2025) and 29.6 (2030). With zero NOM it would reach 30.6, and age-cost growth would still be 2.11%. Migration mostly dilutes cost per person.

**Standstill.** Scale age-related programs by CPI × age-cost population, which is about 1.4pp a year above CPI × population.

## Regressions (associations, not causal)

Each outcome is regressed on 4-quarter NOM as a % of population, with Newey-West HAC (6 lags). Cells show the coefficient (t-stat).

| y | Sample | Lag 0 | Sum lags 0–4 |
|---|---|---|---|
| Rent CPI y/y | 1982–2026 | 2.81 (3.1) | 2.92 (2.6) |
| Rent CPI y/y | 2006Q3–2026 | 4.14 (6.0) | 6.27 (8.5) |
| Rent CPI y/y | 2006Q3–2019 | 8.00 (3.9) | 12.0 (8.1) |
| Real GDP pc y/y | 1982–2026 | −1.96 (−4.5) | −2.21 (−5.1) |
| Real GDP pc y/y | 2006Q3–2026 | −1.55 (−2.5) | −0.83 (−1.5) |

A NOM rate 1pp higher (about 280k people) goes with rent inflation about 3–8pp higher and GDP-per-capita growth about 1–2pp lower. Part of that is mechanical, because a coefficient of −1 comes from the denominator alone. Common cycles are not controlled for.
