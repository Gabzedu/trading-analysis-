# Trading Study Analysis (2023–2024)

## Project Overview

This project analyzes my personal trading activity during my early trading study period, covering trades recorded between 2023 and 2024, before I shifted focus to Data Analytics.

The goal is to investigate execution quality and decision-making during this beginning phase, focusing on the gap between planned and actual outcomes rather than overall profitability — and to apply a real data cleaning and analysis workflow to a messy, real-world dataset.

---

## Data Description

The dataset contains manually recorded trading data collected between January 2023 and August 2024, originally spread across two separate Excel files (one per year) and merged into a single dataset for this analysis.

Key characteristics and data quality notes:

- This was my first structured trading journal. The raw data contained manual entry inconsistencies: inconsistent capitalization (W/w, Long/long), typos in date fields (e.g. "Mario" instead of "Março", a double space in one date), and a mix of account/environment categories.
- 7 trades had no W/L result recorded. These were inferred from the sign of the net profit (positive → W, negative → L) rather than dropped, since the financial outcome was available even though the label was missing.
- The `RRR Realized` field in the original spreadsheet was on a different scale than `RRR Planned` and not directly comparable. The correct realized RRR was recalculated as `net profit / risk in euros`, confirmed against trades that closed exactly at take-profit.
- Data covers 2023–2024 only. No 2022 or 2025 records were available for this project.
- Account/environment types were grouped into three categories — **Backtesting**, **Demo**, and **Live Funded Account** — to avoid mixing risk-free simulation with real capital when comparing performance.

---

## Objectives

- Compare planned vs. realized Risk-Reward Ratio (RRR)
- Evaluate performance by account/environment type
- Investigate whether performance changes immediately after a losing trade (post-loss sequence)

---

## Tools & Technologies

- Python (Pandas, NumPy, Matplotlib)
- Google Colab
- Excel

---

## Phase 1 – Planned vs. Realized RRR

<p align="center">
  <img src="visuals/rrr_planned_vs_realized.png" alt="Planned vs Realized RRR" width="700">
</p>

**Key Insights:**
- Planned RRR ranged from 2.4 to 3.0 across all environments — the trading strategy itself has a
