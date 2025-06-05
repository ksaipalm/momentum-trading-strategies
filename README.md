# Momentum Indicators Backtesting Project

This project explores the use of momentum indicators—**RSI**, **MACD**, and the **Stochastic Oscillator**—to generate trading signals and evaluate their effectiveness through backtesting. It is a hands-on application of concepts in quantitative finance and algorithmic trading.

## Overview

Using Python in a Jupyter Notebook (via the Anaconda distribution), this project:
- Retrieves historical stock data using `yfinance`
- Applies momentum-based trading strategies
- Simulates realistic trading behavior by shifting trading signals forward one day
- Calculates and visualizes cumulative returns of the strategy vs. a buy-and-hold benchmark
- Exports results as charts and CSV files for further analysis

## Technical Indicators

- **Relative Strength Index (RSI):** Measures recent price movement magnitude to identify overbought (>70) or oversold (<30) conditions.
- **Moving Average Convergence Divergence (MACD):** Compares short- and long-term EMAs to indicate trend shifts via crossovers.
- **Stochastic Oscillator:** Compares the closing price to its recent range using %K and %D lines, with crossovers signaling trend changes.

## Methodology

1. **Environment & Tools:**
   - Jupyter Notebook (via Anaconda)
   - Python packages: `yfinance`, `pandas`, `matplotlib`, `ta`

2. **Steps:**
   - Set parameters: ticker symbol, momentum indicator, start and end dates
   - Download historical price data using `yfinance`
   - Apply chosen momentum indicator (RSI, MACD, or Stochastic) using the `ta` package
   - Generate buy/sell signals and compute daily/strategy returns
   - Simulate execution with `.shift(1)` to reflect trade on the next day
   - Plot and compare cumulative returns for the strategy vs. buy-and-hold
   - Save plot and dataset as PNG and CSV

## Example Configuration (in code)

```python
# Data Parameters
ticker = 'VVOS'
indicator = 'Stochastic'
start_date = '2015-01-01'
end_date = '2025-01-01'
```

## How to Use

1. **Clone the repository** (or download the ZIP):
   ```bash
   git clone https://github.com/yourusername/momentum-indicators-backtest.git
   cd momentum-indicators-backtest
   ```

2. **Open the Jupyter Notebook** using Anaconda or any compatible Python environment:
   ```bash
   jupyter notebook mom_ind.ipynb
   ```

3. **Modify the input variables** in the notebook as needed:
   - `ticker` (e.g., `'AAPL'`, `'TSLA'`, `'VVOS'`)
   - `indicator` (`'RSI'`, `'MACD'`, or `'Stochastic'`)
   - `start_date` and `end_date` (e.g., `'2015-01-01'` to `'2025-01-01'`)

4. **Run all cells** to:
   - Fetch historical stock data
   - Apply the selected momentum indicator
   - Generate buy/sell signals
   - Simulate strategy execution
   - Plot and save the equity curve
   - Export the results as `.csv` and `.png` files

5. **Review the outputs**:
   - The equity curve image will be saved as:  
     `TICKER_INDICATOR_backtest_chart.png`
   - The full dataset (including signals and returns) will be saved as:  
     `TICKER_INDICATOR_backtest.csv`
