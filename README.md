## Time Series Forecasting for Airline Flight Departure Delays Using Long Short Term Memory (LSTM) Neural Networks (To be updated soon)


![](image/airport.png)


## Aim

Air Traveling has been increasingly integrated into our daily life.  Like driving, it is essential to plan ahead and anticipate possible or imminent delays.  This study aims to predict future flight departure time delays using long short-term memory (LSTM) neural network models.  The data was published by the Bureau of Transportation Statistics of the US Department of Transporation, and is available at: https://www.kaggle.com/yuanyuwendymu/airline-delay-and-cancellation-data-2009-2018.


## Methods

1. Exploratory Data Analysis

    I. Extract data and identify features.

    II. Clean and manipulate data

    III. Plot distribution and determine correlations
    

2. Modeling

    Recurrent neural network.  LSTM models were implmented using Tensorflow-Keras.  The representative summary of the neural network was shown on Table 1.  Models have different number of bidirectional layers and LSTM units.  Different optimizer learning rate and epochs were used to achieve best mean squared error (MSE) and mean absolute percentage error (MAPE).

3. Time Series
    The monthly dataset was split into train and test sets, 80:20.  A sliding window of previous 66 months were used to predict future 24 months.  Lag time = 1.

## Exploratory Data Analysis

The dataset contains total of 60+ million rows and 27 columns from 2009 to 2018.


Figure 1.  Flight departure from 2009 to 2018.  (A) Delayed and on-time departure. (B) Delayed departure and arrival. (C) Histogram of delayed time.  (D) Averaged delayed time.

A)

![](image/flightDeparture2009_2018.png)

B)

![](image/delayedDeparture2009_2018.png)

C, D)

![](image/time_delay.png)



Figure 2.  Delayed departure time.  (A) Type of delays.  NAS = National Aviation System.  (B) Time of a day.

A)

![](image/boxplotDelay.png)

B)

![](image/boxplotTime.png)



Figure 3.  Flight departure during the months between 2009 and 2018.  (A) Delayed and on-time departure.  (B) Delayed departure time.

A)

![](image/months.png)

B)

![](image/boxplotMonths.png)



Figure 4.  Flight departure for airline companies between 2009 and 2018.  (A) Total number of flights for each airline.  (B) Delayed and on-time departure.  (C) Delayed departure time.

A)

![](image/airline_counts.png)

B)

![](image/airline.png)

C)

![](image/boxplotAirline.png)



Figure 5.  Flight departure in US States/Districts/Territories between 2009 and 2018.  (A) Delayed and on-time departure.  (B) Delayed departure time.

A)

![](image/states.png)

B)

![](image/boxplotStates.png)



Figure 6.  Correlation matrix of delayed flight departure information.

![](image/correlation_matrix.png)



## LSTM Model

Table 1.  A representative LSTM model summary.

![](image/LSTM_model_summary.jpg)

Figure 7.  A representative schematic of LSTM architecture.


![](image/schematic_LSTM_architecture.jpg)



## Time Series

Figure 8.  Time series plot of averaged monthly delayed departure time for all airlines.  (A) Representative test prediction (crimson).  (B) Future prediction (light crimson).  n = 3, standard deviation with 95% confidence interval.

A)
![](image/predict_test_all_flights.png)

B)
![](image/predict_future_spread_all_flights.png)


Figure 9.  Time series plot of averaged monthly delayed departure time for Southwest Airlines.  (A) Representative test prediction (crimson).  (B) Future prediction (light crimson).  n = 3, standard deviation with 95% confidence interval.

A)
![](image/predict_test_sw.png)

B)
![](image/predict_future_spread_sw.png)


Figure 10.  Time series plot of averaged monthly delayed departure time for Alaska Airlines.  (A) Representative test prediction (crimson).  (B) Future prediction (light crimson).  n = 3, standard deviation with 95% confidence interval.

A)
![](image/predict_test_alaska.png)

B)
![](image/predict_future_spread_alaska.png)


Table 2.  Time series test prediction result (n = 3).

![](image/result_table.jpg)


## Next Steps
LSTM nerual network models were built and used to perdict flight departure time delay in this study.  The univariate models consist of multiple bidirectional LSTM layers and has an overall performance of MAPE ranging from 10.0 ± 0.1% to 11.5 ± 0.8% on predictions.  Future directions may consider multivariate LSTM models and develop a web application for the flight departure information using FLASK.


## Technologies

![](image/technologies.jpg)


## Acknowledgements

I would like to thank L Belenky, S English, K Boerstler, and J Hall for their help and discussion...

