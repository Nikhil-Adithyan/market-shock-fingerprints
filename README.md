# Market Shock Fingerprints

A small Python event-study notebook for comparing how different market shocks show up across prices, options skew, correlations, and sentiment.

This is not a prediction model. It is a descriptive analysis of how markets repriced around three different events that are often grouped under broad labels like risk or geopolitical risk.

## What this is

The notebook compares three market events:

- Oct 2023 Middle East shock
- Aug 2024 yen carry / liquidity shock
- Apr 2025 tariff shock

The goal is to see whether different shocks leave different market fingerprints across assets, volatility, options skew, safe-haven behavior, and sentiment.

## What the notebook measures

The analysis looks at:

- Cross-asset repricing around each event
- T+1 absolute move rankings
- SPY options implied-volatility skew
- SPY / GLD rolling correlation
- A simple composite stress score
- News sentiment where available
- Heatmaps comparing event-level behavior across assets

## Main idea

The same broad risk label can hide very different market mechanisms.

In this notebook:

- The Oct 2023 event behaved more like a limited confidence shock.
- The Aug 2024 event looked more like a liquidity and volatility shock.
- The Apr 2025 tariff event produced broader structural repricing across sectors and asset classes.

The point is not that these labels are perfect. The point is that market shocks can be compared by their actual repricing behavior instead of by headline category alone.

## Repository contents

```text
README.md
final code notebook.ipynb
```

The notebook contains the full code and saved outputs used in the analysis.

## How to use this

Open the notebook:

```text
final code notebook.ipynb
```

You can read through the saved outputs directly, or rerun the notebook if you have access to the required market data.

To rerun the analysis from scratch, install the basic Python packages used in the notebook:

```bash
pip install pandas numpy requests plotly matplotlib seaborn scipy
```

Then add your own market data API key inside the notebook where the data-fetching section is defined.

## Data notes

The notebook uses market data for ETFs, volatility products, options chains, and news sentiment around selected event windows.

The analysis depends on the availability and structure of the data returned by the provider. Some sections, especially options skew and sentiment, may vary depending on coverage, plan limits, and historical availability.

## Limitations

This is a descriptive event-study notebook, not a trading system.

A few important caveats:

- The events are hand-selected.
- The sample size is small.
- The composite stress score is meant for comparison inside this analysis, not as a universal market-risk indicator.
- Options skew can be sensitive to available strikes, expiries, and data coverage.
- Sentiment is used as a secondary comparison layer, not as a standalone signal.
- The analysis does not claim to forecast future shocks.

## Why this exists

Market commentary often compresses very different events into broad labels like geopolitical risk, macro shock, or risk-off.

This notebook takes a more mechanical approach: look at what moved, how fast it moved, which assets absorbed the shock, whether options markets repriced ahead of time, and whether sentiment moved before or after prices.

## Full writeup

The full article version is available here:

[Geopolitical Risk Is a Lazy Label. The Market Prices the Shock Underneath](https://www.insightbig.com/post/geopolitical-risk-is-a-lazy-label-the-market-prices-the-shock-underneath)
