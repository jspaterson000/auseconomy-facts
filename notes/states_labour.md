# States' finances and labour-market detail

Code: `src/auseconomy/states_labour.py`; tests: `tests/test_states_labour.py`. Fiscal data: PBO National Fiscal Outlook 2026-27 (general government sector; outcomes to 2024-25, 2025-26 estimate, forecasts to 2029-30; NSW and WA adjusted by the PBO). Labour: ABS Data API, seasonally adjusted.

**Net debt.** Combined national net debt (Cth, states and local, transfers eliminated) is $920bn in 2025-26 (31.0% of GDP) and reaches $1,279bn by 2029-30 (36.5%). From 2024-25 the Commonwealth adds $253bn and the states $235bn (the national total is slightly lower after eliminations). Queensland is the outlier: $15bn to $98bn, or 2.8% to 14.6% of GSP. Victoria adds $62bn (to $199bn, still the largest, 24% of GSP), NSW $46bn, SA $21bn. WA is nearly flat and stays below 7% of GSP.

**Share of public spending.** On own-purpose spending (excluding grants between governments), the states are 50.3% of Cth plus state spending in 2024-25 (NSW 14.2%, VIC 12.8%, QLD 10.8%), down from 52.8% in 2019-20. Gross expenses ($464bn states, $812bn Cth in 2025-26) double count about $165bn of Cth grants, so they can't be added. States made 63% of net capital investment in 2024-25 and 53% by 2029-30 as the Cth share rises (2025-26 is distorted by a large Victorian asset transfer). State interest costs double, $17bn to $35bn.

**Underutilisation.** The rate is 10.9% in 2026 Q3, against 13.5% in 2019 Q4, but up from 10.1% in 2025 Q4. Unemployment is 4.6% and underemployment 6.3% (8.3% in 2019). Vacancies are 325k, about 0.45 per unemployed person, versus a vacancy rate near 2.0% in 2026 H1 (3.0% in 2022). Hours per worker are 31.3 a week, versus 31.8 in 2019 Q4.

**Where jobs growth came from.** Filled jobs rose 2.27m between 2019 Q4 and 2026 Q2. Non-market industries (health care and social assistance, education, public administration and safety) account for 50% of that growth (+1.14m, up 31%) and 49% of hours growth, from only 26% of jobs in 2019. Health care and social assistance alone is 32% (+728k, up 39%). Market industries grew 11%, led by construction (+206k) and retail (+196k).

**Gaps and caveats.**
- ABS GFS annual (5512.0) not fetched; the PBO series are built from it. There is no GFS dataflow in the Data API.
- The industry split is by industry, not sector: private schools, private hospitals and NDIS providers sit in "non-market"; public enterprises sit in "market".
- No state-level labour breakdown.
- The 2025-26 Final Budget Outcome (Sep 2026) is not reflected for the states; the state-own forecast vintages are in `state_budget_vintages`.
- Local government is not separated.
- Vacancy rate is blank for 2026 Q3 because the Labour Account ends in Q2.
