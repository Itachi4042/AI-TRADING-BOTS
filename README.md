# AI-TRADING-BOTS
In this project, I developed a rule-based AI trading strategy that detects high-probability trade entries based on technical indicators (EMA and candlestick patterns), and enhanced it with hyperparameter optimization and machine learning techniques.

The strategy uses 9 EMA and 15 EMA to determine trend strength and direction. A long or short trade is triggered when the price touches these EMAs and forms a valid bullish or bearish candle, with strict wick/body ratio filters (e.g., Marubozu or Pin Bar candles). The angle of the EMAs (measured in degrees) is also used as a trend confirmation signal.

I implemented a grid search to optimize the following key hyperparameters:

Upper wick % for bullish candles (5–10%)

Lower wick % for bearish candles (5–20%)

EMA angle thresholds (30° to 45° upward/downward)

Risk-to-reward ratios (1.5R, 2R, 2.5R, 3R)

The strategy was backtested on 10 NIFTY 50 stocks over 3 timeframes (5m, 15m, 1h) using historical OHLC data from the NSE via OpenChart. Each combination was evaluated on trade count, winrate, and profitability. The best-performing configurations were selected automatically.

Finally, the results were visualized using Seaborn/Matplotlib, including heatmaps of winrate by hyperparameter, and clean line plots showing winrate vs trade frequency for each RR ratio.

