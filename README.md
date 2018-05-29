# STA-664-Final-Project
Comparative Analysis of Spatial and Temporal Models on PM2.5 Concentration in Beijing

Team member:
Chunxiao Li, Xuetong Li

# File documentation

Final_Report.html: The final report

Final_Report.Rmd: The rmd file with all codes

.Rdata and .rds: Files to shorten runtime

cleaned_data: Cleaned and transformed datasets

Beijing_District: Shape files

Beijing_17: Raw datasets

# Project introduction

In order to build a spatial-temporal model to predict PM2.5 in Beijing, we collect the air quality data and meteorology data from 2017-01-31 to 2018-01-31 in several monitoring stations in Beijing. In addition, in order to analyze the Beijing air pollutants in the district scale, we also get the geographical boundaries data of all the districts in Beijing.

In order to analyze PM2.5 in the time series scale, we pick one of the most busy districts in Beijing, Haidian, where most of the univeristies in Beijing locate, as our target district.

## Temporal

The temporal models we fitted includes:

Hourly ARIMA model, 

Daily ARIMA model, 

Daily Gaussian Process	model, 

Daily linear regression model with Gaussian Process residual, 

Daily Random Forest model.

## Areal

In order to build the spatial models, we pick 2017-10-03 as our target date, and try to fit spatial models (areal and point reference) for the PM2.5 concentration. The PM2.5 concentration in each station points and the average PM2.5 of all the stations in each districts are calculated respectively.

The areal spatial models we fitted includes:

CAR (Conditionally autoregressive) model,

SAR (simultaneous autoregressive) model,

Bayesian CAR model,

Bayesian SAR	model,

Linear regression using air quality data with CAR residual,

Linear regression using air quality and meteorology data with CAR residual.

## Point reference 

The point reference models we fitted includes:

Thin Plate Splines model,

Spatial Gaussian Process model using JAGS,

Spatial Gaussian Process model using spBayes.

## Spatial-temporal Model

And finally a Spatial-temporal Model is fitted. In order to build a spatial-temporal model, we use monthly average data of all the air pollutants in each air quality stations by averaging all the observations thoughout each month.
