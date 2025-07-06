# Stock Prices Time Series Forecasting

This project demonstrates a comprehensive workflow for time series forecasting using stock market data. The notebook leverages Python libraries such as `yfinance`, `statsmodels`, and `scikit-learn` to fetch historical stock prices, fit forecasting models, generate predictions, and visualize results.

## Features

- **Data Fetching:** Automatically downloads historical stock data for selected symbols using Yahoo Finance.
- **Modeling:** Supports ARIMA, Exponential Smoothing, and ensemble forecasting methods.
- **Forecasting:** Predicts future stock prices for a user-defined horizon (e.g., 30 days).
- **Evaluation:** Calculates predicted returns and provides recommendations based on forecasted performance.
- **Visualization:** Plots historical prices, forecasts, and comparative bar charts of predicted returns.
- **Analysis:** Offers summary statistics and risk analysis for the forecasted stocks.

## Workflow Overview

1. **Import Libraries:** Loads all necessary Python packages.
2. **Initialization:** Sets up the `StockForecaster` class and configuration.
3. **Data Fetching:** Downloads and preprocesses stock data.
4. **Model Fitting:** Fits ARIMA and Exponential Smoothing models.
5. **Forecasting:** Generates forecasts using selected methods.
6. **Evaluation & Visualization:** Summarizes results and visualizes forecasts.
7. **Additional Analysis:** Provides risk and return analysis.

## Usage

1. **Clone the repository or download the notebook.**
2. **Install dependencies:**
    ```bash
    pip install pandas numpy yfinance statsmodels scikit-learn matplotlib seaborn
    ```
3. **Open the notebook:**  
   Run the notebook in Jupyter or VS Code.
4. **Configure symbols and parameters:**  
   Edit the `symbols`, `period`, and `forecast_days` as needed.
5. **Run all cells:**  
   The notebook will fetch data, fit models, generate forecasts, and display results.

## Example

```python
symbols = ['AAPL', 'MSFT', 'GOOGL', 'AMZN', 'TSLA']
forecaster = StockForecaster(symbols=symbols, period='1y', forecast_days=30)
forecaster.fetch_data()
forecaster.generate_forecasts(method='ensemble')
forecaster.print_summary()
forecaster.plot_forecasts()