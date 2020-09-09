# Time_Series_Forecasting
Covering the basic aspects of Time Series Analysis and Forecasting

## ***A***uto***R***egressive Model

A Linear Model, where the current period values are a sum of past outcomes (lagged values) multiplied by a numeric factor.  


### $ x_t = C + φ x_{t-1} + ε_t$  

- $x_t-1$: The values of X during the previous period.  
- $φ$ :  Any numeric constant by which we multiply the lagged values. (-1 < φ < +1)    
- $ε_t$ : The residual, difference between our prediction for period t and the correct value.

AR(1): $ x_t = C + φ_1 x_{t-1} + ε_t$  
AR(2): $ x_t = C + φ_1 x_{t-1} + φ_2 x_{t-2}+ ε_t$   

*More Lags ---> More Complicated ---> More Coefficients ---> More Likely Not Significant*

## ***M***oving***A***verage Model

A Linear Model, where the current period values are a sum of past errors multiplied by a numeric factor.  


### $ r_t = c + θ ε_{t-1} + ε_t$  

- $ r_t$: The values of 'r' in the current period.
- $θ$ :  A numeric coefficient for the value associated with the lag.    
- $ε_t$ : The residual, difference between our prediction for period t and the correct value.
- $ε_{t-1}$ : The residuals for past values.

MA(1): $ r_t = C + θ_1 ε_{t-1} + ε_t$  
MA(2): $ r_t = C + θ_1 ε_{t-1} + θ_2 ε_{t-2}+ ε_t$   

## ***A***uto***R***egressive***M***oving***A***verage  
This is a combination of both the above models.

### $ r_t = c + φ_1 r_{t-1} + θ_1 ε_{t-1} + ε_t$

## ***A***uto***R***egressive***I***ntegrated***M***oving***A***verage  
The only difference between ARIMA and ARMA is the “integrated” part. Integrated refers to the number of times needed to difference a series in order to achieve stationarity, which is required for ARMA models to be valid. So we can either feed a stationary series to the ARIMA and add the differencing factor, or drop it by feeding the stationarised series.

### $ △ P_t = c + φ_1 △ P_{t-1} + θ_1 ε_{t-1} + ε_t$

