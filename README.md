# Multi-Asset Portfolio Risk and Performance Report

## Project overview

This project downloads five years of market data for US equities, technology equities, long-term Treasury bonds, gold and Bitcoin. 
It creates a diversified portfolio and evaluates both the individual assets and the combined portfolio using return, volatility and downside-risk measures.

## Why the project matters in finance

Portfolio decisions should not be based on return alone. Analysts also need to understand volatility, drawdowns, tail losses, correlations and the amount of portfolio risk contributed by each holding. 
This project converts raw market prices into a concise investment-risk report.

## Skills demonstrated

- Automatic market-data collection with `yfinance`
- Financial return and portfolio calculations
- Risk-adjusted performance measurement
- Downside-risk and tail-risk analysis
- Correlation and diversification analysis
- Matplotlib reporting and reproducible CSV outputs

- ## Models, ratios and analytics

- Total and annualised return
- Annualised volatility
- Sharpe, Sortino and Calmar ratios
- Maximum drawdown
- Historical 95% VaR and CVaR
- Rolling 63-day volatility
- Asset-return correlation
- Component contribution to portfolio volatility

- ## Data source

- The primary source is Yahoo Finance through `yfinance`. The selected tickers are SPY, QQQ, TLT, GLD and BTC-USD. If the public download is unavailable, the script uses clearly labelled, reproducible demonstration prices so the workflow can still be tested without a manual upload.

## Running the project

```bash
python main.py
```

The script also works in Jupyter or Google Colab. Install the requirements, paste or run `main.py`, and execute the workflow. No CSV upload or API key is required.

## Outputs

The `outputs/` folder contains:

- Adjusted prices and daily returns
- Portfolio daily returns
- Performance and risk KPI table
- Correlation matrix
- Risk-contribution table
- Cumulative-return chart
- Drawdown chart
- Rolling-volatility chart
- Correlation heatmap
- Portfolio risk-contribution chart

## Interpreting the results

The performance table shows whether higher returns were accompanied by higher volatility or deeper drawdowns. Sharpe and Sortino ratios measure return relative to total and downside risk. VaR and CVaR estimate ordinary and average severe daily losses. The risk-contribution table highlights holdings whose share of total portfolio risk is materially larger than their capital weight.

## Limitations

- The weights are fixed and treated as if rebalanced daily.
- Transaction costs, taxes and management fees are excluded.
- Historical VaR assumes the sample represents future market conditions.
- Correlations and volatility can change during periods of stress.
- The demonstration fallback is not real market evidence.

## Future improvements

- Add monthly rather than daily rebalancing.
- Include transaction costs and portfolio turnover.
- Compare alternative portfolio allocations.
- Add benchmark-relative performance measures.
- Export a formatted Excel management report.
