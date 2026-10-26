# Housing supply, prices and the Accord (`housing.py`)

**Data.** ABS API `BUILDING_ACTIVITY` (8752.0, to Jun-q 2026), `RES_DWELL_ST`, `CPI` (rents 30014, new dwellings 97559); 8731.0 Aug-2026 Table 6 (SA approvals); ERP from `macro_quarterly`.

## National Housing Accord (1.2m homes, Jul-2024 to Jun-2029)

| | |
|---|---|
| Completions, 8 quarters to Jun-2026 (SA) | **355,817** (original 356,010) |
| Straight-line target to date | 480,000 (60k a quarter); gap −124,183; 74% of path |
| Required for the remaining 12 quarters | **70,349 a quarter (281k a year)** |
| Latest 4-quarter pace | 180,546 a year (45k a quarter) |
| Projected total at that pace | **≈897k** (75% of target) |

This is close to the NHSAC's *State of the Housing System 2026*: about 862k net supply against about 900k underlying demand.

**Pipeline.** In the Jun-q 2026 (SA):
- completions were 47,168 (+15.9% y/y);
- commencements were 52,201 (+14.4%);
- approvals were 53,052, the highest since Sep-q 2021.

Commencements over the year (204k) exceed completions (180k), and 248,733 units under construction is a series high. More completions are coming, but not 70k a quarter.

**Supply relative to population.** Completions were 6.4 per 1,000 residents in the year to Jun-2026, against a 1985-2019 average of 7.9. The Dec-2025 and Mar-2026 readings (6.2) are the lowest since 1981. Population grew 2.5 persons per completion (2010-19 average: 2.1).

**Prices and costs (Jun-q 2026, y/y).**
- Mean dwelling price: $1.10m, +6.9% (+60% since Dec-2019).
- CPI rents: +3.5%, down from a 7.8% peak in Mar-2024. Real rents are now −0.4% y/y. Rents are +24.4% since Dec-2019, against CPI +26.8%.
- New-dwelling purchase costs: +5.4%, re-accelerating from 0.7% in Jun-2025, and +46.7% since Dec-2019.

**Caveats**
- **Accord count.** Total completions, including alterations and conversions; nothing tests "well-located", and demolitions are not netted off.
- **SA versus original** cumulative totals differ by about 200; the Accord convention is SA.
- **The price index** is the mean price of the stock, not quality-adjusted (the RPPI ended in 2021).
- **CPI rents** cover existing leases and lag advertised rents. Sep-q CPI is due 28 Oct.
- **Jun-2026 population** is extrapolated (ERP ends Mar-2026). The API's corrupt SA "Total Residential, total work" completions series (around 27 million) is excluded.
