# HW Week 11 addendum
Below are the answers to the associated questions for this homework assignment.

## The questions and the answers:

1. How does the Prophet Algorithm differ from an LSTM? Why does an LSTM have poor performance against ARIMA and Prophet for Time Series?

 - The Prophet algorithm is different from an LSTM because an LSTM is based on neural networks, while Prophet is a formula 
containing only four terms: for the trend, seasonality, holidays, and errors. LSTM can have poor performance against ARIMA 
and Prophet for time series forecasting (e.g., stock prediction) because it is prone to overfitting. This is especially true
for small datasets, and the issue cannot easily be solved dropout or other forms of regularization. LSTM is better suited to very
large datasets where we want to uncover complex patterns.

2. What is exponential smoothing and why is it used in Time Series Forecasting?

 - Exponential smoothing is an averaging technique to reduce the variation of (smooth) time series data. The technique 
is called exponential smoothing because the weights of the current and previous data points in the average are calculated
based on an exponential function (1 - weight)^n. It is used in Time Series Forecasting to get the general trend from noisy data
by removing (smoothing out) the noise.


3. What is stationarity? What is seasonality? Why Is Stationarity Important in Time Series Forecasting?

 - Stationarity is when a time series is not affected by the time of the measurement. In contrast, seasonality is when a time
series is affected by the time of the measurement. An simple example of seasonality is the average monthly temperature of a 
town. This measurement has a yearly seasonality, since (for the northern hemisphere) temperatures are warmer in the summer and
colder in the winter. When a time series has seasonality, the measurement will be affected by trends and seasons. These are 
important concepts in time series forecasting because it is useful to break out each component that contributes to the time 
series so that they can be analyzed and predicted separately. If a model understands and can predict these components, then 
future predictions will be more accurate.


4. How is seasonality different from cyclicality? Fill in the blanks: ___ is predictable, whereas ___ is not.

 - Seasonality is observed over the calendar year, while cyclicality are effects that may last longer (or shorter) and could 
be related to other effects that come and go (i.e., have cycles). Seasonality is predictable, whereas cyclicality is not.

