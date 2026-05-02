An autoregressive integrated moving average model predicts a time series by a relationship between the error terms and the lagged observations. 

<a id='forecast'></a> 
## Getting started with the ARIMA model

You can use the `ARIMA` method from the `statsmodels` library to forecast a time series using the ARIMA model. You already know how to import `ARIMA` method.

Using the `ARIMA` method, the ARIMA model can be trained as
```python
ARIMA(data, (p, d, q))
```

where 
* p is the AR parameter.
* d is the difference parameter. This is I in ARIMA, the number of times you need to difference the series to make it stationary.
* q is the MA parameter.

### Steps followed: 

1. Read The data 
2. Use ADF test : the ADF test which states the null hypothesis that the time series is not stationary. If the p-value < 0.05, you reject the null hypothesis.
3. If series is not stationary: to convert a non-stationary series into a stationary one, you can apply the differencing technique.
4. From the PACF/ACF plot significant spike you will get parameters p and q.
5. Use the liabiray and fit the ARIMA model to obtain forcasted value.
