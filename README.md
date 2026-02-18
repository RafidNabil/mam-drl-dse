# MAM-DRL Reproducibility

Data for: *Trading Policy Optimization Using Deep Reinforcement Learning for the Dhaka Stock Exchange* (QPAIN 2025)

## Data
- **Source**: Dhaka Stock Exchange official portal (https://www.dsebd.org/)
- **Period**: 2013-01-01 to 2022-12-31
- **Stocks**: 30 DSE stocks handpicked for complete OHLCV data coverage
- **Format**: `data/[TICKER].csv` with columns: `Date,Open,High,Low,Close,Volume`

## Experimental Splits
| Phase | Period | Purpose |
|-------|--------|---------|
| DRL Training | 2013-01-01 to 2015-12-31 | Train A2C, DDPG, PPO agents |
| Meta-Training | 2016-01-01 to 2018-12-31 | Learn mixture weights |
| Meta-Testing | 2019-01-01 to 2022-12-31 | Out-of-sample evaluation |

## Files
- `data/` — 30 CSV files, one per stock (e.g., `ACI.csv`)
- `stock_list.txt` — List of the 30 ticker symbols used

## Notes
- Prices are adjusted closing prices from DSE.
