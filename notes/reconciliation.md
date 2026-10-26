# Policy decisions vs parameter variations

Built by `auseconomy.reconciliation`. The policy/parameter split comes from the PBO's *Historical budget forecasts and measures* (2026-27 edition). I checked it against 828 figures from the Budget papers (BP1 CSV/DOCX/PDF, MYEFO PDFs) for 32 updates. The largest difference was $1m. In every year, previous UCB + changes = new UCB to within $2m.

## Forecast errors (actual − forecast, % of forecast)

Total expenses as published at each update, 2008-09 Budget onward. Pre-COVID = outcomes up to 2018-19. The t-statistics use Newey-West standard errors on target-year means.

| horizon | pre-COVID mean (MAE) | post-COVID mean (MAE) |
|---|---|---|
| 1 yr | +2.1% (2.4%), t=1.8 | +9.8% (9.8%), t=3.1 |
| 2 yr | +2.0% (2.9%), t=1.2 | +13.3% (13.3%), t=5.8 |
| 3 yr | +1.3% (3.5%), t=0.6 | +16.6% (16.6%), t=28 |

- **Before COVID there was no significant bias.** The +2% average comes from 2009-10 to 2013-14. For 2014-15 to 2018-19 forecasts ran slightly high (−0.2%, −0.7%, −1.5%).
- **Since COVID spending has come in well above forecast**, by $57b, $80b and $100b on average. This holds even for outcomes from 2022-23 to 2025-26 (+5.7%, +11.0%, +16.2%).
- **Payments look the same:** +1.5%, +1.4%, +1.1% pre-COVID; +8.1%, +10.9%, +14.0% post-COVID.
- **By function the post-COVID misses are broad.** Health was +11% to +16% (about +2% pre-COVID). Social security and welfare was +8% to +15% (−2% to −6% pre-COVID). The pre-COVID function sample covers only 2014-15 to 2018-19.

## Revisions since the 2023-24 Budget

Seven updates (2023-24 MYEFO to 2026-27 Budget), summed over 2023-24 to 2026-27:

- **Payments +$143.0b:** policy $73.6b (51%), parameter $69.3b (49%).
- **Receipts +$178.7b:** almost all parameter ($178.1b). On the UCB, policy cost $73.1b and parameters added $108.8b.
- **Expenses +$184.6b:**
  - policy $80.7b (44%)
  - program-specific parameters $88.4b (48%): demand growth, not decisions
  - economic parameters $20.4b: prices and wages $8.5b, unemployment $4.8b, GST $6.0b
  - debt interest $4.2b; other −$9.2b

Payments changes by update:

| update | policy | parameter |
|---|---|---|
| 2023-24 MYEFO | +$6.5b | +$21.3b |
| 2024-25 Budget | +$32.5b | +$11.2b |
| 2024-25 MYEFO | +$19.1b | +$23.0b |
| 2025-26 Budget | +$20.7b | −$28.0b |
| 2025-26 MYEFO | −$3.8b | +$35.1b |
| 2026-27 Budget | +$0.5b | +$4.5b |

Example: 2025-26 payments were first published at $687.0b (March 2022). By the 2026-27 Budget they were $788.1b: +$51.3b policy, +$49.7b parameter. The outcome was $786.6b.

## Biggest policy additions (named measures, payments)

These exclude the "decisions not yet announced" lines ($5–8b at most updates).

- **2023-24 Budget:** Strengthening Medicare $5.7b; working-age payments $4.9b; GST compliance $3.8b.
- **2023-24 MYEFO:** PBS listings $3.5b.
- **2024-25 Budget:** Defence Strategy $5.7b; Energy Bill Relief $3.5b; PBS $3.4b.
- **2024-25 MYEFO:** early educator pay $3.6b; PBS $2.5b.
- **2025-26 Budget:** Strengthening Medicare $8.4b; infrastructure $1.8b.
- **2025-26 MYEFO:** PBS $1.8b; mental health $1.1b.
- **2026-27 Budget:** hospital funding (NHRA) $18.1b; Defence Strategy $6.8b; PBS $5.9b. Savings largely offset these: the net effect is +$8.7b in 2026-27 and −$11.0b in 2029-30.

## Caveats

- **PBO workbooks only start at the 2021-22 MYEFO.** Its first two editions contain no estimates.
- **2013-14 to March 2022 vintages are function level only.** They come from Budget-paper tables and tie to total expenses within $4m.
- **PBO MYEFO editions have no sub-function estimates**, so `is_it_a_cut()` compares sub-functions Budget to Budget.
- **The policy split exists only for aggregates.** `is_it_a_cut(keywords=...)` lists matching measures instead.
