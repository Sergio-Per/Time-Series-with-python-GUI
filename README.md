

## **Time-Series Analysis with Python and Graphical User Interfaces**

#### by Sérgio Pereira, April 2022 - Final Project - Data Science, Concordia University
Graphical User Interfaces for Time-Series Analysis (including Descriptive Statistics, Spectral Analysis and Predictive modelling with different models) 

A time-series is used in this project to code in python and explore a comprehensive set of statistical analysis, modeling, and prediction tools. These, combined with Interactive GUIs, allow the user to perform different actions on the data. For example, the user can select time periods or specific days and statistical parameters are computed and visualized; in the predictive models changes in hyperparameters are shown in the prediction curve plotted.

This notebook is expected to have some regular development at least for two reasons: (i) because the topic of time series is interesting and important in so many fields; (ii) this kind of notebook, with interactive widgets, convinced me on the interest of these GUIs for educational purposes in mathematics, statistics, programming, or science in general. A time-series is a sequence of measurements from a system that varies in time. Usually, these information points are collected at adjacent time-spaces, thus there is a relation between observations, proportional or not. This is a characteristic of time-series that differentiates them from other data. For coding purposes, a time-series is a set of data indexed by time. Use case: Hourly data of Black Carbon (BC) mass concentration measurements from a small city (60000 in) are used throughout this notebook. Thus, this is a univariate time series, a sequence of measurements of the same variable. BC aerosols emerge in the atmosphere mainly produced by anthropogenic activities, with vehicles, industry, and biomass burning being the most important sources. Section 1 deals essentially with descriptive statistics and main features of the data; in section 2 some further analysis is made, including the time-series autocorrelation and stationarity. Section 3 introduces the frequency domain with spectral analysis and shows some features of Fourier analysis. Section 4 brings machine learning techniques, and different predictive models are implemented and applied in the time-series.

# **1. Descriptive Statistics**

![alt text](https://github.com/Sergio-Per/Time-Series-GUI/blob/main/GUI%201.png)

# **2. Autocorrelation, Stationarity, Resampling**

![alt text](https://github.com/Sergio-Per/Time-Series-GUI/blob/main/GUI%202.png)

# **3. Frequency Domain, Spectral Analysis, FFT, High-Pass/Low-Pass filters**

![alt text](https://github.com/Sergio-Per/Time-Series-GUI/blob/main/GUI%20Filters.png)

![alt text](https://github.com/Sergio-Per/Time-Series-GUI/blob/main/GUI%20Fourier.png)

# **4. Time series forecasting/Machine Learning**

The forecasting process consists of predicting future values of a time series, either by modeling the series based on its previously observed patterns (autoregressive) or by using other external variables. The former approach is to be adopted with the univariate BC measurements.

Three different models are briefly explored: ARIMA/SARIMAX as well as Random Forest and Lasso regressors were used to create forecasters, including grid search with backtesting (cross-validation method applied to previous periods) to identify the best combination of lags and hyperparameters for the models.
In the following subsections each model is trained, and the best combination of parameters is selected and presented. The predictions can be computed and visualized with these best parameters or other values can be selected with the predictions being updated accordingly.

Briefly, Lasso is a Linear Model trained with L1 regularization and it estimates sparse coefficients. The alpha parameter controls the degree of sparsity of the estimated coefficients. A random forest is a meta estimator that fits a number of classifying decision trees on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting. The sub-sample size is controlled with the max_samples parameter if bootstrap=True (default), otherwise the whole dataset is used to build each tree. SARIMAX (Seasonal Auto-Regressive Integrated Moving Average with eXogenous factors) is an extension of the ARIMA class of models. ARIMA models compose 2 parts: the autoregressive term (AR) and the moving-average term (MA)
