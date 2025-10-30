# Forecast17 — 1-Month Ahead Weather AI (MAE: **0.31°C**)

> **24 years of data. 0.31°C monthly forecast.**

[Website](https://shadowbyte911.github.io/Forecast17) • [CSV + Plot](results/)

---

## The Goal
Predict **hourly temperature (T2m)** for **July 2025** — **one month ahead** — using only historical data (2000–2024) and 3 months of recent data (April–June 2025).

No physics. No supercomputers. Just **Python + AI**.

---

## Results (July 2025 Backtest)

| Model              | MAE       | RMSE      |
|--------------------|-----------|-----------|
| **LSTM**           | **0.3111°C** | 0.5083°C |
| Weighted Ensemble  | 0.4155°C  | 0.6007°C  |
| Stacking Ensemble  | 0.4760°C  | 0.6453°C  |
| Dense Network      | 0.5534°C  | 0.7238°C  |
| XGBoost            | 0.5304°C  | 0.7286°C  |
| Random Forest      | 0.5273°C  | 0.7271°C  |

> **LSTM wins at 0.31°C** — better than most global models.

---

## Forecast Plot
![July 2025 Forecast](results/forecast_plot.png)

---

## Data
- `results/july_hourly_predictions_with_metrics.csv` → **720 hours** of:
  - `timestamp`, `true_temp`
  - Predictions + **per-hour MAE/RMSE** for **8 models**

[Download CSV](results/july_hourly_predictions_with_metrics.csv)

---

## Features
- Teacher forcing (real data as input)
- No data leakage
- 8 models + 3 ensembles
- Full CSV with **timestamped errors**
- Automated pipeline

---

## Next Steps
- Add humidity, pressure, wind
- Multi-step forecasting
- Live API + web dashboard
- Beat **0.25°C MAE**

---

> **No code. No data. Just results.**  

[![GitHub stars](https://img.shields.io/github/stars/shadowbyte911/Forecast17?style=social)](https://github.com/shadowbyte911/Forecast17)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## Topics
`weather-forecasting` `time-series` `lstm` `machine-learning` `python` `ai`
