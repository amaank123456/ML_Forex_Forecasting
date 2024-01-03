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

## How to run VARIMA models
- All of the VARIMA models are Jupyter notebooks named "VARIMA_[currency_rate].ipynb. For example, the VARIMA model for predicting the USD/EUR rate is VARIMA_usd_eur.ipynb. Run any of these notebooks to test the models

## How to test older models
- The older models, such as the support vector regression, ridge regression, ARIMA models, etc. are all stored in the old folder.

## Results
\begin{table*}[h]
\caption{Mean Squared Errors of Testing Set}
\label{mse_test}
\begin{tabularx}{\textwidth}{@{} l *{10}{C} c @{}}
\toprule
Models
& USD/EUR & EUR/CHF & EUR/GBP & GBP/CHF & USD/CHF 
& USD/GBP \\ 
\midrule
VARIMA  & 1.4322e-04 & 4.6296e-05 & \textbf{5.3731e-06} & \textbf{1.9925e-06} &  \textbf{2.3364e-05}
& 3.4806e-05\\
ARIMA     & 3.7204e-05   & 5.5789-05   & 1.5508e-05   & 7.0519e-05   & 3.2726e-05   & \textbf{2.1932e-05}\\
SVR     & \textbf{3.4495e-05}   & \textbf{1.7669e-05}   & 2.8602e-05   & 4.3797e-05   & 3.7837e-05   & 5.0576e-05\\ 
Ridge Reg     & 1.6929e-04   & 7.1149e-04   & 1.9277e-04   & 3.4109e-03   & 1.2450-03   & 1.9865-04\\
RF     & 7.7606e-05   & 1.2043e-04   & 1.4847e-05   & 1.6205e-04   & 8.4769e-04   & 1.2910e-04\\
\bottomrule
\end{tabularx}
\end{table*}

### Acknowledgements
The VARIMA scripts make use of code from [1] for implementing the Augmented Dickey Fuller (ADF) and the Grangers Causality Test. These code snippets were solely used to determine necessary attributes of underlying data before training the models
[1] Prabhakaran, S. (2022, August 30). Vector autoregression (VAR) - comprehensive guide with examples in Python. Machine Learning Plus. https://www.machinelearningplus.com/time-series/vector-autoregression-examples-python/ 
