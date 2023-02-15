# Time Series Models
A time series is a sequence of numbers that are ordered by a time index.
## Time Series Breakdown
A time series can be broken down into the following components:
### Trend Component 
A trend is a consistent directional movement in a time series. These trends will be either deterministic or stochastic. The former allows us to provide an underlying 
rationale for the trend, while the latter is a random feature of a series . Trends often appear in financial series, and many trading models use sophisticated trend 
identification algorithms.
### Seasonal Component
Many time series contain seasonal variation. This is particularly true in series representing business sales or climate levels. In quantitative finance we often see
seasonal variation, particularly in series related to holiday seasons or annual temperature variation (such as natural gas).
### Remainder component 
Part of the time series not captured by seasonal or trend component.

We can write the components of a time series y<sub>t</sub> as :
<br>
y<sub>t</sub> = S<sub>t</sub> + T<sub>t</sub> + R<sub>t</sub>
<br>
where 
<br>
S<sub>t</sub> is the seasonal component 
<br>
T<sub>t</sub> is the trend component 
<br>
R<sub>t</sub> is the remainder component of the time series.

## Autocorrelation and Stationarity
### Autocorrelation
Autocorrelation is the similarity between observations as a function of the time lag between them. Such relationships can be modeled using an autoregression model. The 
term autoregression indicates that it is a regression of the variable against itself. In an autoregression model, we forecast the variable of interest using a linear
combination of past values of the variable. Thus, an autoregressive model of order p can be written as :
<br>
y<sub>t</sub> = c + ϕ<sub>1</sub> y<sub>t - 1</sub> + ϕ<sub>2</sub> y<sub>t - 2</sub> + ....ϕ<sub>p</sub> y<sub>t - p</sub> + ϵ
<br>
where ϵ<sub>t</sub> is white noise.

### Stationarity
A time series is said to be stationary if its statistical properties do not change over time. Thus a time series with trend or with seasonality is not stationary, as 
the trend and seasonality will affect the value of the time series at different times. On the other hand, a white noise(A white noise process is a random process of 
random variables that are uncorrelated and have a mean of zero and a finite variance) series is stationary, as it does not matter when you observe it, it should look 
similar at any point in time.
<br>
<br>
<br>
In order to use time series forecasting models, we generally convert any nonstationary series to a stationary series, making it easier to model since statistical 
properties don't change over time.


### Differencing
Differencing is one of the methods used to make a time series stationary. In this method, we compute the difference of consecutive terms in the series. Differencing is
typically performed to get rid of the varying mean. Differencing can be written as:
<br>
y'<sub>t</sub> = y<sub>t</sub> - y<sub>t - 1</sub> 
<br>
where y<sub>t</sub> is the value at a time t.
<br>
When the differenced series is white noise, the original series is referred to as a non-stationary series of degree one.

