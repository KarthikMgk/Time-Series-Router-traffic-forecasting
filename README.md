## Time-Series-Router-traffic-forecasting
The problem is to forecast the router traffic given its historical data. This is a time series problem as you know. The dataset consists of router traffic data from 1/10/2018 to 2/11/2018 for 5 router/network devices. Our task is to build a model which identifies the patterns of 5 of those network devices and to forecast traffic seperately for the next 2 or 3 days. 

This problem was a part of my internship interview at CanGo Networks pvt ltd, Chennai.

## Overview of dataset
Dataset was given by CanGo Networks pvt ltd. It consists of KPI, ne_date, ne_id, ne_hour, metric and the value. Here value is our predictor variable. There are 5 network devices in the data for which we will have to forecast their value for the next 2 or 3 days. Dataset has 3600 odd records and 6 features

![image](https://user-images.githubusercontent.com/35063929/57911106-7e460b00-78a4-11e9-9510-d6ff2fe5d301.png)

## Techniques I tried
I started with AR and Arima since we had hourly predictions for a month. But unfortunately, both of these models were not able to capture the dynamics in the data. Hence I posed this as a regression problem, I created some more features and did regression using XGBoost regressor and the results were great!

## Evaluation Criteria
I used MSE and MAE as metrics for this problem since we are regresing the data


## Resources
I used kaggle, google and some stackexchanges to get help from as usual
