# STAT390-Snowman
Snowman Project Group for STAT 390 (Daniel He, Asher Bank, Willem Luyten)

## Introduction:

Throughout the COVID-19 pandemic, spikes in case numbers and hospitalizations put significant strain on hospitals and communities across the country. The goal of this project is to predict the number of COVID-19 cases in a given state on a given day as well as examine the causes underlying days with significantly higher COVID-19 case numbers. The ability to better understand and predict these increases in COVID-19 cases including where, when, and why these spikes occur would allow government and healthcare officials to more efficiently allocate resources to help mitigate the effects of future spikes.

## Modeling: 

In this repository you will find the time series models, along with (for multivariate models) their feature selection: 
- ARIMA
- Seasonal ARIMA
- Auto-ARIMA
- Prophet (both Univariate and Multivariate)
- XGBoost

They are modeled on our dataset comprising covid information on covid-reporting, environental, political, location date for the top 10 US states by population. We limit our prediction from January 2022 to April 2022, predicting on data from March 2020 to December 2021. 

## Our specific objectives and goals for this project are as follows:
- Create a time-series model that accurately and precisely predicts the number of Covid cases and deaths using at least 50 features (as outlined in the section below) in a specific county on a given day
- Create graphs mapping the predicted and actual cases in a given county through a given period to allow further analysis on which periods would be considered “spikes”
- Identify crucial predictors of Covid “spikes” and discuss how easy it would be to manipulate and track these predictors in order to allow healthcare providers and decision-makers better foresight around and control of future spikes
