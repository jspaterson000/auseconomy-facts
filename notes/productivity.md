# Productivity (`productivity.py`)

**Data.** ABS API `ANA_AGG`, `ANA_IND_GVA`, `LABOUR_ACCT_Q`; *ASNA 2025-26* (23 Oct 2026); 5260.0.55.002 (2024-25). Log growth a year; "2010-19" = 2009-10→2018-19.

**Benchmarks reproduced exactly.** Market-sector LP / MFP / capital deepening are 1.85 / 0.29 / 1.56 (2004-05→14-15) and 0.57 / 0.39 / 0.19 (2014-15→24-25) (PC). Jun-2014→Jun-2026 GVA per hour: non-market −2.7% (PC −2.5%), market +7.5%.

| % a year | 2010-19 | 2019-26 | change |
|---|---|---|---|
| GDP per hour worked | 1.07 | 0.16 | −0.91 |
| Market-sector LP | 1.52 | 0.52 | −1.00 |
| … MFP | 0.62 | 0.33 | −0.29 |
| … capital deepening | 0.91 | 0.19 | **−0.72** |
| 19-industry LP (shift-share) | 1.18 | 0.21 | −0.97 |
| … within-industry | 1.05 | −0.07 | −1.12 |
| …… mining | 0.20 | −0.59 | −0.79 |
| … hours reallocation | 0.13 | 0.28 | +0.15 |
| …… into non-market (O, P, Q) | −0.11 | −0.19 | **−0.08** |

**Composition is minor.** Health care's hours share rose from 11.4% to 13.9%, at 0.75× average nominal output per hour. The extra care-economy drag is **about 0.08 pt a year, roughly 8% of the slowdown**. Without mining, the slowdown is 0.25 pt (0.89→0.64), of which the care economy is 0.04 pt (14%). The slowdown is overwhelmingly within industries: real output per hour fell in mining, construction and utilities, and grew more slowly elsewhere in the market sector.

**Capital deepening is about 72% of the market-sector slowdown**, MFP about 28%. Capital services growth fell from 3.2% to 1.8% a year while hours growth rose (1.15%→1.3%).

**Latest year (2025-26).** GDP per hour +0.6% (2024-25: −0.6%); market LP +0.9%, MFP +0.7%.

**Caveats**
- **Mining's weight.** Its price-driven VA share (12.9% against 2.0% of hours) inflates both its within drag and the offsetting reallocation; check the ex-mining run.
- **Non-market output** is largely input-measured, so health and education productivity is near zero by construction.
- **Vintages.** 5260.0 runs to 2024-25; 2025-26 comes from ASNA Table 13 (1 dp). ASNA revises 2023-24 LP from 0.96 to 0.5 (`*_asna`), giving 2019-26 market LP of 0.41 and MFP of 0.26.
- **Hours** follow ASNA Table 15. On Labour Account hours (which diverge after 2019), 2019-26 within is +0.02 and reallocation +0.20.
- **Gaps.** Industry MFP ends 2024-25. Real unit labour costs (trend only) are missing from 2018-19 to 2022-23.
