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
where 
<br>
S<sub>t</sub> is the seasonal component, T<sub>t</sub> is the trend component, R<sub>t</sub> is the remainder component of the time series.

## Autocorrelation and Stationarity
### Autocorrelation
Autocorrelation is the similarity between observations as a function of the time lag between them. Such relationships can be modeled using an autoregression model. The 
term autoregression indicates that it is a regression of the variable against itself. In an autoregression model, we forecast the variable of interest using a linear
combination of past values of the variable. Thus, an autoregressive model of order p can be written as
<br>
y<sub>t</sub> = c + ϕ<sub>1</sub> y<sub>t - 1</sub> + ϕ<sub>2</sub> y<sub>t - 2</sub> + ....ϕ<sub>p</sub> y<sub>t - p</sub> + ϵ

- 
