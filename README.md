# Project2 - Natural Gas Forecasting/Scheduling

This machine learning model will help natural gas supplier/scheduler prepare for better inventory controls in future. These kind of machine learning tool can come up with automated forecasting models and allow one person to do the work of multiple data scientists.

---

## Project Overview

Using time series forecasting models, develop a machine learning model to forecast natural gas pricing and consumption based on 10 years of historical data. Further, develop a correlation table (and/or heatmap) which contains the correlations between following variables: natural gas price, natural gas consumption, natural gas exports, storage and ambient temperature.                                                                                                               

The following two time series forecasting models were used: 1) Prophet 2) ARIMA

---

## Data Resources/Basis

#### Natural Gas Data:
- Price, Consumption, Storage, Exports
- U.S. Energy Information Administration (www.eia.gov)


#### USA Average Temperature Data:
- National Centers for Environmental Information (ncei.noaa.gov)

#### Historical Data:
- 10 Years(2012-2022)

#### Forecast Data:
- 3 Years

---

## Usage

Ensure the conda dev environment is activated.

Please launch jupyter lab to run files following files:

- ng_correlation.ipynb - Natural gas trends and correlations/heatmap
- arima_forecast.ipynb - Times Series Forecasting using ARIMA

Open Google Colab (https://colab.research.google.com/) and upload the following starter notebook:
- prophet_ngforecasting.ipynb - Times Series Forecasting using Prophet

All the csv files to run the models are located in the Resources folder.

---

## Identifying Patterns and Correlations/Heatmap

Useful insights can be gained from the quantitative plots. The dip in Apple (AAPL) stock is due to split of shares during that period. Amazon (AMZN) stock has performed better than AAPL during last 3 yrs data. The Sharpe ratio shows the gain in relation to the risk. The returns have gone higher for both stocks after Covid pandemic. The quantitative analysis plots are as follows:

### Natural Gas Spot and Futures Prices (NYMEX) - Daily
<img src="Images/dailyprice.png" width="650" height="300">

### Gas & Temperature Monthly Trends
<img src="Images/correlation.png" width="650" height="300">

### Heatmap
<img src="Images/heatmap.png" width="400" height="300">

---

## Time Series Forecasting Analysis

Monte Carlo algorithm is used to predict future stock values. Past stock values downloaded using Alpaca APIs are used to create a normal distribution of past daily returns. MC algorithm uses past daily return normal distribution to predict future daily values and cumulative returns by randomly selecting values from the distribution and propagating the stock's current value into the future. Cumulative returns are calculated from the future stock values and plotted for 500 simulations. All simulations are numerically different from each other due to the randomly selected daily return values from the normal distribution. Cumulative return probability distribution is also shown as a bar graph to illustrate the most probable future scenario range from all 500 simulations. 95% Confidence interval and its boundary values are also given for information. These boundary values should be evaluated together with the future cumulative return distribution. The financial forecasting analysis plots are as follows:

### Summary of Prophet and ARIMA forecasting models 
<img src="Images/prophet_arima_comparison.png" width="650" height="350">

---

## Issues

Waiting for Onur to send the csv file issues while dealing with ARIMA model. 

---

## New Library

New library "ARIMA" was used. An ARIMA model is a class of statistical models for analyzing and forecasting time series data. ARIMA is short for "AutoRegressive Integrated Moving Average". Any ‘non-seasonal’ time series that exhibits patterns and is not a random white noise can be modeled with ARIMA models. If a time series, has seasonal patterns, then you need to add seasonal terms and it becomes SARIMA, short for ‘Seasonal ARIMA’. 

---

## Presentation

Please click on the following link to view the project presentation.
https://github.com/paragmb/Project2/blob/main/Presentation/FinTech_Project2_Grp3_Presentation.pdf

---

## Future Steps

Machine learning model for natural gas consumption can be updated monthly. Machine learning model for natural gas can be updated daily/weekly. Although Henry Hub (HH) spot prices were used in this time series forecasting analysis, an additional model using the domestic gas prices can also be developed. Impact of LNG exports in next 3 to 5 years can be further studied and incorporated in the natural gas forecasting scenarios. 


---

## Contributors

Bolaji Ajimotokan, Onur Guvener, Parag Borkar

---

© 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
