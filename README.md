# NIFTY 50 Momentum Backtesting Engine

## About

This project is a simple backtesting engine built in Python to test a momentum-based trading strategy on the NIFTY 50 index. It uses a 50-day and 200-day Simple Moving Average (SMA) crossover to generate buy and sell signals and compares the strategy's performance with a buy-and-hold approach.

The goal of this project was to understand the basics of quantitative trading, strategy backtesting, and performance evaluation using historical market data.



## Features

* Downloads historical NIFTY 50 data using Yahoo Finance
* Calculates 50-day and 200-day moving averages
* Generates trading signals based on SMA crossovers
* Avoids look-ahead bias by shifting trading signals
* Computes daily and cumulative returns
* Calculates:

  * Annualized Return
  * Sharpe Ratio
  * Maximum Drawdown
* Compares the strategy against a buy-and-hold benchmark
* Visualizes price trends, returns, and drawdown



## Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* yfinance


## Strategy

The strategy is based on a simple moving average crossover.

* Enter a trade when the 50-day SMA moves above the 200-day SMA.
* Exit the trade when the 50-day SMA falls below the 200-day SMA.

To keep the backtest realistic, trading signals are shifted by one day so that today's signal is executed on the next trading day.



## Results

Backtest Period: **2019–2024**

| Metric            |       Value |
| ----------------- | ----------: |
| Annualized Return |   **4.90%** |
| Buy & Hold Return |  **15.96%** |
| Sharpe Ratio      |    **0.40** |
| Maximum Drawdown  | **-36.48%** |



## Project Structure

```text
NIFTY-50-Momentum-Backtesting/
│
├── backtest.ipynb
├── strategy_results.csv
├── nifty_backtest.png
├── README.md
└── requirements.txt
```


## Installation

Install the required libraries:

```bash
pip install pandas numpy matplotlib yfinance
```



## Running the Project

Run the notebook from top to bottom. It will:

1. Download historical market data
2. Generate trading signals
3. Backtest the strategy
4. Calculate performance metrics
5. Plot the results
6. Save the output chart and CSV file



## Future Improvements

Some ideas to extend this project:

* Include transaction costs
* Test different moving average combinations
* Add technical indicators like RSI or MACD
* Backtest on other indices or stocks
* Compare multiple strategies




