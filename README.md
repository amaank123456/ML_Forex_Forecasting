# Description
This is the final project for my Machine Learning for Signal Processing course where we attempted to predict foreign exchange (FOREX) currency exchange rates using machine learning/statistical models.

# Introduction
Foreign exchange (FOREX) currency rate forecasting is the process of predicting future exchange
rates between two currencies based upon recent currency data and related, predictive factors. FOREX
forecasting, moreover, presents lucrative trading opportunities to traders if they can accurately
predict and arbitrage changes in currency rates. Achieving this, however, is made difficult due to
the intrinsic volatility of exchange rate and their dependence on daily political and socioeconomic
events. As such, numerous statistical and machine learning methods have been deployed to approach
this problem. Previous work evaluated the prediction accuracy of numerous statistical
and machine learning methods including Support Vector Regression (SVR), decision trees, random
forests, ridge regressions, and Autoregressive Integrated Moving Average (ARIMA). Preliminary
results indicated that ARIMA was the best performing model. Later work evaluated the prediction accuracy
of Vector Autoregressive Integrated Moving Average (VARIMA) models trained using related
time-series data, such as stock index and gold prices. The VARIMA models’ prediction accuracy
was evaluated on their ability to predict the daily closing prices of USD/EUR, USG/GBP, USD/CHF,
EUR/GBP, EUR/CHF, and GBP/CHF currency rates.

# Dataset
1. USD/EUR:
https://finance.yahoo.com/quote/USDEUR%3DX/history?p=USDEUR%253DX
2. USD/GBP:
https://finance.yahoo.com/quote/USDGBP%3DX/history?p=USDGBP%253DX
3. USD/CHF:
https://finance.yahoo.com/quote/USDCHF%3DX/history?p=USDCHF%253DX
4. EUR/GBP:
https://finance.yahoo.com/quote/EURGBP%3DX/history?p=EURGBP%253DX
5. GBP/CHF:
https://finance.yahoo.com/quote/GBPCHF%3DX/history?p=GBPCHF%253DX
6. EUR/CHF:
https://finance.yahoo.com/quote/EURCHF%3DX/history?p=EURCHF%3DX
7. Gold Price:
https://finance.yahoo.com/quote/GC%3DF/history?p=GC%253DF
8. Standard & Poor's 500 (S&P 500):
https://finance.yahoo.com/quote/%5EGSPC/history?p=%255EGSPC
9. Financial Times Stock Exchange 100 (FTSE 100):
https://finance.yahoo.com/quote/%5EFTSE/history?p=%255EFTSE
10. EURO STOXX 50:
https://finance.yahoo.com/quote/%5ESTOXX50E/history?p=%255ESTOXX50E
11. Swiss Market Index (SMI):
https://finance.yahoo.com/quote/%5ESSMI/history?p=%255ESSMI

# How to run VARIMA models
- All of the VARIMA models are Jupyter notebooks named "VARIMA_[currency_rate].ipynb. For example, the VARIMA model for predicting the USD/EUR rate is VARIMA_usd_eur.ipynb. Run any of these notebooks to test the models

# How to test older models
- The older models, such as the support vector regression, ridge regression, ARIMA models, etc. are all stored in the old folder.

# Results
Mean Squared Errors of Testing Set for Rates from 12/04/2023 to 12/08/2023

| Models | USD/EUR    | EUR/CHF    | EUR/GBP    | GBP/CHF    | USD/CHF    | USD/GBP    |
| ------ |:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|
| VARIMA | 1.4322e-04 | 4.6296e-05 | 5.3731e-06 | 1.9925e-06 | 2.3364e-05 | 3.4806e-05 |

# Contributors
- Amaan Kazi
- Satvik Dixit
- Aryan Singhal
- Justin Dannemiller
- Jionghao Han

# Acknowledgements
The VARIMA scripts make use of code from [1] for implementing the Augmented Dickey Fuller (ADF) and the Grangers Causality Test. These code snippets were solely used to determine necessary attributes of underlying data before training the models
[1] Prabhakaran, S. (2022, August 30). Vector autoregression (VAR) - comprehensive guide with examples in Python. Machine Learning Plus. https://www.machinelearningplus.com/time-series/vector-autoregression-examples-python/ 
