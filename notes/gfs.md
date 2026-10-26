# Quarterly Commonwealth GFS and inflation channels

**Built.** `gfs.py`: the ABS Data API has no GFS dataflow, and each release covers only the financial year
to date. So the history is stitched from all 91 release workbooks (Dec 2003 to Jun 2026) at the latest vintage:
2002Q3 to 2026Q2 for Commonwealth, all-levels and state & local general government. It also adds ABS 5206.0
Table 17 (all-levels cash social benefits, seasonally adjusted, 1959 on). Tables: `gfs_quarterly` (tidy) and
`fiscal_impulse` (Commonwealth: % GDP, y/y growth, impulse = −Δ4 primary balance in % of GDP).
`inflation_channels.py` swaps each channel, one at a time, into the public-demand slot of `inflation.py`'s
tests. The baseline reproduces `findings.md`.

**Caveats.**
- The ABS publishes no seasonally adjusted GFS. The "derived" seasonally adjusted rows are our own STL
  adjustment, and the analysis uses y/y growth instead.
- "Transfers to households" is GFS *other current transfers*: mostly cash benefits. **NDIS and other
  in-kind benefits are under non-employee expenses.**
- GFS does not apply AASB 15/16/1058/1059, and timing differs from the budget. Commonwealth expenses still
  match PBO accrual expenses within 1.4% for 2015-16 to 2023-24, but **2024-25 is −3.8%** (probably one-offs
  booked in different years).
- The GFS sample is 2004Q3 to 2026Q2: n=88, or 77 ex-COVID (channel observations 2020Q1 to 2021Q4 dropped).

**Findings.** HAC s.e. in brackets, per 1pp of the channel. Real means CPI-deflated. LP is average
trimmed-mean inflation over t+1..t+h.

| channel | Phillips sum of lags (p) | LP h=4 | LP h=8 |
|---|---|---|---|
| Public demand, 1994+ | 0.068 (0.045) p=0.13 | 0.012 (0.034) | 0.024 (0.027) |
| Public demand, GFS sample | 0.068 (0.055) p=0.22 | 0.003 (0.038) | 0.018 (0.030) |
| **Cth transfers, real** | **0.023 (0.008) p=0.002** | 0.011 (0.007) p=0.13 | 0.011 (0.007) p=0.14 |
| ↳ ex-COVID | 0.000 (0.009) p=1.00 | 0.009 (0.007) | 0.005 (0.006) |
| Cash benefits, all levels, 1994+ | 0.024 (0.007) p<0.001 | 0.007 (0.006) | 0.008 (0.007) |
| ↳ ex-COVID | 0.015 (0.010) p=0.12 | 0.008 (0.007) | 0.004 (0.006) |
| Cth consumption proxy | 0.024 (0.020) p=0.23 | 0.025 (0.022) | 0.025 (0.015) |
| Cth government final consumption (national accounts) | 0.064 (0.037) p=0.08 | −0.016 (0.037) | 0.000 (0.027) |
| Cth grants | 0.008 (0.022) p=0.72 | −0.005 (0.011) | −0.015 (0.008) |
| Cth total expenses | 0.015 (0.016) p=0.35 | 0.001 (0.020) | −0.003 (0.017) |
| Fiscal impulse (pp GDP) | 0.037 (0.069) p=0.59 | −0.256 (0.135) p=0.06 | −0.051 (0.124) |
| ↳ ex-COVID | −0.067 (0.079) p=0.40 | 0.204 (0.130) p=0.12 | **0.270 (0.105) p=0.010** |

- **Transfers are the only significant Phillips-curve channel, and only because of COVID.** One s.d.
  (12.7pp) predicts +0.29pp of inflation. Without 2020-21 the effect is zero. Granger p is 0.020 to 0.035, but
  it comes from lags of opposite sign, which is timing rather than a lasting effect.
- Consumption, grants and total expenses show nothing robust, like public demand.
- **Fiscal impulse:** it Granger-causes inflation on the full sample (HAC p<0.001) but not ex-COVID
  (p=0.71). Ex-COVID, 1pp of GDP goes with +0.27pp inflation at h=8. That is one horizon among about 240 LP
  estimates, and the sign flips on the full sample. Treat it as a hypothesis for out-of-sample testing.
- Fiscal flows react to the cycle, so these are associations, not causal effects.
