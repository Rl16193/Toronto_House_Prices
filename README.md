# Toronto_House_Price

## Data

We delve into the task of predicting housing prices in Toronto using different models. The dataset used is sourced from the Canada Mortgage and Housing Corporation (CMHC) and covers the housing market data for the last 4 years. Specifically, we focus on apartments and townhouses in Toronto. The average size of Toronto houses is approximately 1600 square feet, which can allow us to analyze the change in rates per square foot.

The housing market data used in this analysis was obtained from the Canada Mortgage and Housing Corporation. You can access the data tables and research reports from their website: CMHC Housing Market Data. https://www.cmhc-schl.gc.ca/en/professionals/housing-markets-data-and-research/housing-data/data-tables/housing-market-data.

To ensure data reliability and accuracy, we consider only the average values of houses sold in new constructions for each month. In cases where insufficient houses were sold or the sale price was confidential, we replace the average value with null. For predictive modeling purposes, we focus on areas with over 40 price values, ensuring a sufficient sample size for robust analysis.


## Stationary and Non-Stationary Data

We begin by conducting the Augmented Dickey-Fuller (ADF) test to determine the stationarity of the data. The housing prices in Toronto are found to be stationary, while the prices in Milton are non-stationary. To handle non-stationary data, we apply data transformations, including the use of the logarithmic function, and employ differencing techniques to make the data stationary.
We applied various models including ARIMA, SARIMA, and RandomForestRegressor to predict housing prices in Toronto and Milton.

## Result

1. Unlike many other locations, Toronto does not exhibit a consistent upward trend in real estate pricing across the entire city. Instead, specific areas within Toronto experience notable variations in pricing trends.

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/96b2e01c-036d-4c12-a70a-cdb145961d6e)

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/baf1af30-f139-4e7f-939d-a55a432df79f)

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/b328641d-1363-4a12-a44d-00bcaae9f2c0)

2. The XGBoost model demonstrated robust performance in predicting housing prices in Toronto, irrespective of the stationarity of the data. Utilizing XGBoost eliminates the need for explicit stationarity checks, simplifying the modeling process.

The mean absolute percentage error (stationary data): 0.0910546488062614

The mean absolute percentage error(non-stationary data): 0.21738003036827325

3. The ARIMA time series model consistently outperformed other models for both stationary and non-stationary data, showcasing its effectiveness in capturing and forecasting housing price patterns in Toronto.

### Stationary Data

1. The SARIMA and ARIMA model has the best performance in the case of stationary data (City of Toronto). The absolute mean percentage error is 0.045 and the root mean square error of 94396.

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/72c75738-0d4f-4347-9821-45814604cc42)

2. The Random Forest Regressor gives a lower mean square error but the absolute mean error and root mean square are higher.

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/70072f02-f223-450c-8256-71743b1c3e01)


### Non-Stationary Data

1. The ARIMA model provides better results in comparison. The root mean square error is 0.097 and the mean absolute percentage error is 1.27

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/9924e977-f328-4f0b-b492-2d3745ef850a)


## Predictions

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/37b94ed9-92c4-4fea-befb-26e2e91beab8)

**House price prediction using Random Forest Regressor**

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/70da1e38-ec66-4c82-8c24-d9f41424bd0b)

**House Price prediction using XGBoost**
