# Bracket creep, 2024-25 to 2029-30

From `src/auseconomy/taxburden.py`. Figures are for residents, on an income-year basis, in nominal $. **Central** = log-linear density within each ATO range, incomes uprated by WPI. **Low/high** = point-mass or endpoint densities, with incomes growing at WPI −0.5pp or WPI +0.9pp. (0.9pp = historical gap between taxable-income-per-lodger and WPI growth).

## Validation (ATO 2023-24, Table 12)
- **Net tax before calibration:** +1.8% ($333.7bn vs $327.8bn).
- **Rate-scale tax:** −0.03%.
- **2010-11 back-cast:** +3.2%.
- **Decile cut-points:** within 0.3–2.2% of ATO Table 16.
- **WATO:** 12.9m recipients (Budget: "over 13m") at a cost of $3.2bn (PBO: $3.0bn).

## (a) Creep since 2024-25

The counterfactual is legislated law with thresholds indexed. Figures are $bn.

| | 2025-26 | 2027-28 | 2029-30 | 5-yr sum |
|---|---|---|---|---|
| CPI-indexed | 5.8 | 15.3 | **26.9** (26.0–28.3) | 79 |
| WPI-indexed | 5.1 | 18.0 | **34.3** (33.3–36.2) | 94 |
| Net of 2026-28 cuts (WPI) | 5.1 | 7.2 | 22.2 | 56 |

By 2029-30 WPI creep is about $1,900 per lodger, or 2.0% of taxable income. The 15% and 14% rate cuts and WATO hand back about $11bn in 2027-28.

## (b) Stealth tax since 2010-11, measured in 2025-26
- **Gross creep:** $63bn (frozen 2010-11 law: 27.8% average rate; indexed: 23.4%), of which policy returned $51bn.
- **Net:** **$12.5bn under CPI indexing and $13.0bn under WPI**, about $750 per lodger. CPI and WPI each rose about 49% over the period, so real wages were flat.

## (c) Distribution
- **2029-30 (WPI):** the top decile pays 30% of creep and decile 9 pays 16%. As a share of income the burden peaks at 3.1–3.3% in deciles 4–5 ($44k–$73k), against 1.7% at the top.
- **Since 2010-11:** deciles 5–6 carry 47% of the net stealth tax. Decile 9 is better off, because Stage 3 moved the 37% threshold to $135k.

## Versus PBO and Treasury
- **PBO average tax rate (MTBO 2026-27, Fig 4-7):** 23.9→25.7% over 2024-25 to 2029-30; ours is 23.95→25.2%.
  - Levels match in 2024-25.
  - In a no-policy-change year the rise is the same: +0.42pp vs PBO's +0.40pp.
  - The gap opens in 2025-26, when PBO has +0.8pp to our +0.36pp. Cash receipts grew 8.3% that year. WPI uprating on a fixed income shape misses composition and non-wage income growth. The high path closes about half the gap.
- **Treasury:** 24.7% in 2027-28; ours is 24.4%. The $1,000 instant deduction is not modelled.
- **PBO "returning creep" estimates:**
  - 2022: $310bn over 10 years (about $85bn in the first five); 2021: $57bn after 10 years; 2024: 24.9% vs 28.5% (0.36pp a year).
  - Our $94bn over 5 years (0.39pp a year) is consistent with all three. PBO holds the average tax rate constant, which matches our WPI case only if incomes grow at WPI.

## Gaps
- Medicare (single thresholds) and SAPTO are handled by calibration, not modelled.
- Non-residents (0.5% of tax) are excluded.
- The 2023-24 lodgment count is incomplete.
- Pre-2012 LITO and Medicare parameters come from records: back-cast LITO is 14% high.
- Forward parameters are Budget through-the-year rates.
- Negative gearing and CGT reforms are not modelled.
