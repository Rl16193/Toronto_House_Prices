# Toronto_House_Prices

## Data

Housing Market Data for the last 4 years was obtained from Canada Mortage and Housing Corporation. https://www.cmhc-schl.gc.ca/en/professionals/housing-markets-data-and-research/housing-data/data-tables/housing-market-data. The type of units included are apartments and townhouses.

The average value of the houses sold, new construction only is listed for each month. Months where insufficient houses where sold or the sale price was confidential we are unable to arrive at an average value. It is replaced with null. Areas with over 40 price values are considered for the predictive model.


## Stationary and Non-Stationary Data

AD Fuller test is conducted to determine this. Housing Prices for Toronto fall under stationary data. Housing prices for Milton fall under non-stationary data.
We use log function to transform the data. We use differencing techniques to make non-stationary data, stationary.
Then we compare ARIMA, SARIMA, RandomForest Regressor models on the house price data.

## Result

1. The City of Toronto does not show a general upward trend that is expected for real estate pricing and observed in a few specific locations. 

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/96b2e01c-036d-4c12-a70a-cdb145961d6e)

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/baf1af30-f139-4e7f-939d-a55a432df79f)

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/b328641d-1363-4a12-a44d-00bcaae9f2c0)

2. The XGBoost model which works on both stationary and non-stationary performs well in both cases. Using this model will avoid the need to check for stationarity.


The mean absolute percentage error (stationary data) : 0.0910546488062614
The mean absolute percentage error(non-stationary data): 0.21738003036827325

### Stationary Data

1. The SARIMA and ARIMA molde has the best performance in case of stationary data (City of Toronto). The absolute mean percentage error is 0.045 and a root mean square error of 94396.

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/72c75738-0d4f-4347-9821-45814604cc42)

2. The Random Forest Regressor gives a lower mean square error but absolute mean error and root mean square is higher.

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/70072f02-f223-450c-8256-71743b1c3e01)


### Non-Stationary Data

1. The SARIMA model provides better result in comparison. The root mean square error is 0.097 and the mean absolute percentage error is 1.27

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/9924e977-f328-4f0b-b492-2d3745ef850a)


## Predictions

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/37b94ed9-92c4-4fea-befb-26e2e91beab8)

**House price prediction using Random Forest Regressor**

![image](https://github.com/Rl16193/Toronto_House_Prices/assets/100053788/70da1e38-ec66-4c82-8c24-d9f41424bd0b)

**House Price prediction using XGBoost**
