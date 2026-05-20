# Time Series Analysis of Public Transportation C-CPI-U
This project applies time series analysis techniques to model and forecast the Chained Consumer Price Index for All Urban Consumers (C-CPI-U) of public transportation in U.S. cities using monthly data from 1990–2007.

## Overview
* Implemented the Box-Jenkins methodology to investigate whether public transportation C-CPI-U can be modeled using seasonal ARIMA (SARIMA) processes
* Performed exploratory time series analysis, including:
  * Seasonal decomposition
  * Trend and stationarity analysis
  * Differencing for seasonality and trend removal
* Used sample ACF and PACF plots for model identification
* Fitted and compared multiple SARIMA models using AICc model selection
* Conducted residual diagnostics and statistical testing, including:
  * Shapiro-Wilk normality tests
  * Box-Pierce tests
  * Ljung-Box tests
  * McLeod-Li tests
* Evaluated forecasting performance on a held-out testing dataset

## Dataset
The dataset contains monthly public transportation C-CPI-U observations from January 1990 to December 2007 obtained from the U.S. Bureau of Labor Statistics.

## Methods
The project explored several SARIMA model configurations after differencing the data to remove seasonality and trend. Candidate models were evaluated using diagnostic checks and residual analysis.
The final selected model was:
SARIMA(3,1,5)(0,1,1)<sub>12<sub>.
​	
 
Although the model achieved reasonable fit metrics, diagnostic testing suggested SARIMA models may not fully capture the structure of the dataset.

## Tools & Libraries
* R (forecast, tidyverse, MASS, qpcR)

## Key Takeaways
* Public transportation C-CPI-U exhibits both seasonality and long-term trend behavior
* SARIMA models captured some temporal structure but struggled to fully satisfy diagnostic assumptions
* Residual diagnostics indicated remaining autocorrelation and nonlinear dependence, suggesting alternative time series approaches may yield better forecasting performance
