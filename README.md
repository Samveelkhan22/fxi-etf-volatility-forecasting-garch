# FXI ETF Volatility Forecasting using GARCH Models

This project is part of an assignment for ECO4051: Financial Econometrics. It focuses on estimating and analyzing the volatility of the **iShares China Large-Cap ETF (FXI)** using log returns, statistical analysis, and GARCH modeling techniques in Python.

## 📈 Objective

To explore and model the time-varying volatility of FXI using:

- Descriptive statistics
- Autocorrelation analysis
- Exponential Moving Average (EMA)
- GARCH(1,1) volatility modeling
- 10-day volatility forecast

## 🧰 Technologies Used

- Python 3
- [yfinance](https://pypi.org/project/yfinance/)
- pandas, numpy, matplotlib
- scipy.stats
- statsmodels
- arch (for GARCH modeling)

## 📊 Key Steps

1. **Download ETF Data**  
   Historical FXI price data was downloaded using the `yfinance` library from 2010 to 2024.

2. **Calculate Log Returns**  
   Returns were calculated using the formula:  
   \[
   R_t = \log \left( \frac{P_t}{P_{t-1}} \right)
   \]

3. **Statistical Summary**  
   Computed mean, standard deviation, skewness, kurtosis, and performed the Jarque-Bera test to assess normality.

4. **Visualizations**  
   Plotted:
   - Close prices
   - Log returns
   - ACF of returns
   - GARCH conditional volatility

5. **GARCH(1,1) Model**  
   Estimated the GARCH model and analyzed the persistence of volatility using α and β coefficients.

6. **Volatility Forecasting**  
   Forecasted conditional variance for the next 10 trading days using the fitted GARCH(1,1) model.

## 📁 Outputs

- `FXI_GARCH_results.csv`: Contains log returns and conditional volatility values.
- Visual plots of returns, ACF, and volatility.
- Console output with summary statistics and GARCH model coefficients.

## 📌 GARCH Model Insights

- **α (alpha):** 0.10
- **β (beta):** 0.88
- **α + β = 0.98** → High volatility persistence, consistent with financial time series behavior.

## 📚 References

- Lecture Notes from ECO4051: Financial Econometrics
- arch Documentation
- LearnPythonWithRune

