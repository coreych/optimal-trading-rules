# optimal-trading-rules
Based on the paper by Peter P. Carr and Marcos Lopez de Prado on "Determining Optimal Trading Rules without Backtesting", this Python script simulates optimal trading strategies using the Ornstein-Uhlenbeck (O-U) process and aims to determine the optimal trading rules, specifically the profit-taking (PT) and stop-loss (SL) levels, without relying on historical backtesting. The O-U process is a mean-reverting stochastic process.

## Key Features:

1. Fetching Real Stock Data: Utilizes yfinance to fetch historical stock price data.
2. Parameter Estimation: Estimates parameters for the O-U process based on real stock data, including mean and standard deviation of log returns.
3. Simulation of Price Movements: Simulates price movements using the O-U process, incorporating the estimated parameters.
4. Optimization of Trading Rules: Evaluates various combinations of PT and SL thresholds to identify the pair that offers the best risk-adjusted return, as indicated by the Sharpe ratio.
5. Progress Tracking: Includes progress bars for each simulation set using tqdm, enhancing the user experience especially for lengthy simulations.

## Note:
1. The stop-loss (SL) level is a threshold for the absolute decrease in the simulated price from its initial value.
2. The profit-taking (PT) level is a threshold for the absolute increase in the simulated price from its initial value.
