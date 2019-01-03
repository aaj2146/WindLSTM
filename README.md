# Deep Learning for Time Series Data - Wind Energy Forecasting using LSTMs

![alt text](https://raw.githubusercontent.com/username/projectname/branch/path/to/img.png)


## Introduction - Problem Set up
In this project we will forecast the power output of a wind farm given local weather and previous values of power output. This is a multivariate time series forecasting problem where the variable that we are predicting, the wind turbine output, hereafter referered to as just 'output' depends on other time series like the local wind speed and wind direction.

To this end, we use publicly available data from [Sotavento Galicia](www.sotaventogalicia.com/en). The data consists of hourly output from an experimental wind-farm in northern Spain consisting of 24 turbines, each with different specifications along with time stamped hyperlocal measurements of wind speed and wind direction. Data is avaliable for the past 14 years (at the time of writing) going back to January 1st 2004. Thus we have about 120,000 rows of data corresponding to 14 seasons of data. This is a perfect set up for a Deep Learning model.

## Methodology
We will experiment with different architectures LSTMs and GRUs for this project. A quick look at the data shows us that there are quite a lot of missing values for the years 2004, 2005 and 2008. Therefore, we will drop these years from the analysis. Subsequently we take the data from 2006 to 2016 (barring 2008) as the training set, the 2017 data as the validation set and 2018 data as the test set.

The results are reproducible and are avaliable in the notebook '14 - Deep Learning on Alternate Data.ipynb' in this repo. The predictions on the test set look as follows: 

![alt text](https://raw.githubusercontent.com/aaj2146/WindLSTM/blob/master/LSTMSpring.png)

For Fall 2018:

![alt text](https://raw.githubusercontent.com/aaj2146/WindLSTM/blob/master/LSTMS.png)
