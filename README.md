# Week 12: Stock Predictor 

## 1. Deliverables included: 
- model.py main.py scripts 
- requiremnts.txt 
- README.md 
- Rubric Questions/Answers 

## 2. Overview

- This assignment consisted in deploying a stock prediction model as a RESTful API using FastAPI to an AWS EC2 instance
running Amazon Linux, on which miniconda was installed to create a stock-predictor conda environment using Python 3.8. 

- Prophet is a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data.

- The original README.md describes how one can trigger and view predictions from the AWS-deployed model via its public IPv4 address from a local machine using the curl command, for example:

```
curl \
>>--header "Content-Type: application/json" \
>>--request POST \
>>--data '{"ticker":"MSFT", "days":7}' \
>>http://3.134.93.125:8000/predict
```

## 3. Rubric Questions 

### Algorithm Understanding 

- How does the Prophet Algorithm differ from an LSTM?

LSTM is an nueral network architecture and Prophet is a type of addative regression model that uses fourier transformations. 

- Why does an LSTM have poor performance against ARIMA and Prophet for Time Series?

LSTM will tend to overfit the model, Prophet is the simplest of the tree but performs well when temporal patterns exsist, ARIMA is simpler than LSTMs and can outperfom them on smaller datasets, but requires significant effort and domain expertise to tune. 



### Interview Readiness

- What is exponential smoothing and why is it used in Time Series Forecasting?

Exponential smoothing is a time series forecasting method for univariate data that can be extended to support data with a systematic trend or seasonal component. It is used in Time Series forecasting becuase predictions are made using weights on past data where older data is weighted using an exponential decreasing weight. 

- What is stationarity? What is seasonality? Why Is Stationarity Important in Time Series Forecasting?

Stationarity is when time series data has a mean and variance that does not change over time. 

Seasonailty happens in time series data where predictabl or reoccuring patterns happen over time. 

Stationairty is important becuase many time series model depend assume relatively fixed statistical properties.

- How is seasonality different from cyclicality? Fill in the blanks:
___ is predictable, whereas ___ is not.

Seasonality is predictable, whereas cyclicality is not. 

Seasonality are observed patterns that happen over fixed times cyclicality are observed patterns that happen over varied times periods. 
