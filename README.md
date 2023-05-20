# Toronto_House_Prices

## Data

Housing Market Data for the last 4 years was obtained from Canada Mortage and Housing Corporation. https://www.cmhc-schl.gc.ca/en/professionals/housing-markets-data-and-research/housing-data/data-tables/housing-market-data. The type of units included are apartments and townhouses.

The average value of the houses sold, new construction only is listed for each month. Months where insufficient houses where sold or the sale price was confidential we are unable to arrive at an average value. It is replaced with null. Areas with over 40 price values are considered for the predictive model.


## Stationary and Non-Stationary Data

AD Fuller test is conducted to determine this. Housing Prices for Toronto fall under stationary data. Housing prices for Milton fall under non-stationary data.
We use log function to transform the data. We use differencing techniques to make non-stationary data, stationary.
Then we compare ARIMA, SARIMA, RandomForest Regressor models on the house price data.

## Result

1. The City of Toronto does not show a general upward trend that is expected for real estate pricing. 

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/a82e9e83-1f25-4f19-816f-2a8f97f0c62e)

### Stationary Data

1. The Random Forest Regressor performs best in case of stationary data for the Toronto House Data. The absolute mean percentage error is 0.04% and a root mean square error of 90353.

2. The SARIMA and ARIMA model give a straight line.  This can occur if the model fails to capture any trends or seasonality in the data or if the input variables do not have a significant impact on the outcome. It could also indicate that the model is too simplistic or that it requires further tuning or adjustments to better capture the underlying patterns in the data.

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/70072f02-f223-450c-8256-71743b1c3e01)

### Non-Stationary Data

1. The SARIMA model gives better accuracy
