# Market Shock Fingerprints

A small Python event-study project for comparing how different market shocks show up across prices, options skew, correlations, and sentiment.

## What this is

This is not a prediction model. It is a descriptive event-study framework.

The project compares three events:
- Oct 2023 Middle East shock
- Aug 2024 yen carry / liquidity shock
- Apr 2025 tariff shock

## What it measures

- Cross-asset normalized repricing
- T+1 absolute move rankings
- SPY put/call implied-volatility skew
- SPY/GLD correlation breakdown
- A simple composite stress score
- News sentiment where available

## Main result

The three events had very different fingerprints:
- Oct 2023 was a limited confidence shock
- Aug 2024 behaved more like a liquidity shock
- Apr 2025 produced broader structural repricing

## Run it

pip install -r requirements.txt
jupyter lab notebooks/market_shock_fingerprints.ipynb

The notebook runs in cached mode by default.
