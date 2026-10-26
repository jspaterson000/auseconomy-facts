# Where will the budget be in 20 years? (`auseconomy.longrun`)

A transparent projection of the Commonwealth budget to 2045-46. It reproduces the 2026-27 Budget to
2029-30 and the PBO MTBO to 2036-37, then uses the 2026 IGR's long-run assumptions (productivity
1.2%, NOM 235k, prices 2.5%, IGR participation and spending pressures).

## Baseline

| % of GDP | 2029-30 | 2035-36 | 2045-46 |
|---|---|---|---|
| UCB | -0.7 | +0.5 | +1.5 |
| Gross debt | 35.6 (peak 35.8 in 2028-29) | 29.8 | 9.9 |
| Net debt | 21.9 (peak) | 16.2 | -2.3 |
| Payments / receipts | 26.2 / 25.5 | 26.4 / 26.9 | 25.2 / 26.7 |

Interest peaks at 5.8% of receipts in 2031-32 and falls to 1.9%. Real GDP per person grows 1.2% a
year, from $106.6k to $136.4k (2025-26 dollars).

The improvement is bracket creep. Personal income tax rises from 13.1% to 14.8% of GDP by 2036-37
(PBO's current-law path). After that, tax is held at the level reached, about 25% of GDP. This
applies the IGR's ceiling convention at the Budget path's level.

## What moves 2045-46 net debt (pp vs baseline)

| Lever | Δ |
|---|---|
| Brackets indexed from 2027-28 | **+23.2** |
| Tax capped at 23.9% / 24.2% from 2032-33 | +17.8 / +13.6 |
| Defence 3.5% / 3.0% of GDP by 2035-36 | +14.2 / +7.5 |
| NDIS 10% / 8% growth (vs 5%) | +11.5 / +5.4 |
| Productivity 0.7% (RBA) / 1.5% | +10.4 / -5.8 |
| Bracket creep never returned | -10.9 |
| NOM 150k / 300k | +5.0 / -3.5 |
| Bond yields +1pp | +3.8 |

**Tax is the biggest lever.** Whether, and how fully, bracket creep is handed back spans about
34pp of GDP. Defence at 3.5%, NDIS growth of 10% and RBA-style productivity each add 10-14pp.
Migration matters less: migrants add both GDP and spending. Only productivity also changes living
standards; at 0.7%, real GDP per person in 2045-46 is about $10,400 lower.

## Against IGR and PBO

- **PBO 2036-37:** UCB +0.85% (PBO +0.9%), gross debt 28.1% (PBO 28.3%). Every year from 2030-31
  to 2036-37 is within 0.15pp on UCB and 0.3pp on debt.
- **IGR baseline:** with the IGR's 24.2% tax cap, the model gives 23.6% gross debt and a UCB of
  -0.15% in 2045-46. The IGR has 24.0% and -0.4%.
- **IGR, tax held at 25.2%:** the IGR gives 11.6% gross debt, close to this baseline (9.9%).
- **IGR productivity ±0.4pp:** the IGR gives 17.2% / 31.3% gross debt; the model gives 16.8% /
  30.9%. The wage link is calibrated to this.
- **Population:** 34.3m in 2045-46 (IGR 34.4m), with 1.45m people aged 85+ (IGR 1.4m).

## Caveats

- **No macro feedback:** fiscal levers don't move GDP, and yields don't respond to debt. NOM has no
  capital dilution, so higher NOM slightly raises GDP per person through participation.
- **The baseline surplus assumes ~25% tax-to-GDP is sustainable.** Past governments have always
  returned bracket creep.
- **NOM effects are about half PBO's per migrant.** Migrants cost the same per head as residents
  for "other" spending, and NDIS growth is a fixed target.
- **Approximations:** the aged-care age profile is approximate (AIHW). Health and aged-care levels
  follow expenses-table definitions; only their growth is calibrated to the IGR. Defence is on a
  payments basis, including capital.
- **Calibrated parameters:** the yield rollover (0.45) and other spending (-0.14% real per capita
  to 2036-37) are fitted to PBO, whose baseline lets terminating programs lapse.
- **Lever timing:** levers start in 2030-31, except bracket indexation, which uses PBO's
  forward-estimates costing. PBO's 10% NDIS scenario starts earlier (+$68b in 2036-37).
- **Hand-entered inputs:** NDIS to 2029-30 (BP1 Table 6.9.2) and the IGR appendix comparators.
