# US Inflation Pressure Analysis

This repository contains a Jupyter notebook that builds a simple, reproducible
macro-analysis pipeline to assess **inflation pressure** in the United States
using public data.

The goal is not forecasting, but **diagnosis**: understanding whether inflation
is elevated, accelerating, or easing, using standard tools commonly found in
institutional macro research.

## What the notebook does

The notebook performs the following steps:

1. **Data ingestion**
   - Downloads US CPI data from the Federal Reserve Economic Data (FRED) database.
   - Uses both headline CPI and core CPI (excluding food and energy).

2. **Inflation measures**
   - Computes **year-on-year (YoY) inflation**, a stable measure used for
     medium-term assessment.
   - Computes **3-month annualized inflation**, a short-term momentum indicator
     that reacts faster to turning points.

3. **Persistence analysis**
   - Estimates a simple persistence proxy using rolling autocorrelation of
     core inflation.
   - This helps distinguish between transitory price movements and more
     persistent inflation dynamics.

4. **Inflation pressure signal**
   - Combines level, momentum, and persistence into a simple rule-based
     “inflation pressure” regime.
   - Produces a clear, interpretable summary suitable for weekly macro commentary.

## How to run the notebook

1. Install the required Python packages:
   ```bash
   pip install pandas numpy matplotlib fredapi
