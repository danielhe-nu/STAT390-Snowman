# STAT390-Snowman
Snowman Project Group for STAT 390 (Daniel He, Asher Bank, Willem Luyten)

**Abstract**

This report investigates the challenge of predicting daily new cases at the state level in the U.S. from March 2020 to April 2022. Utilizing datasets from various sources including the New York Times, CDC, and U.S. Census Bureau, the study narrows its focus from county to state-level predictions to eventually the top 10 most populous states. Through extensive data preparation, feature engineering, and the ap- plication of ARIMA, prophet, and XGBoost models, the research aims to provide insights into the dynamics of Covid-19 case surges and the factors influencing them.

*Keywords—COVID-19, time-series, ARIMA, prophet, XGBoost*

**Project Overview:** 

Throughout the Covid-19 pandemic, there were several significant spikes in Covid cases and deaths in urban and rural areas around the country. Thus, the goal of our project is to examine these spikes by developing a time series model that predicts the number of deaths and cases in a 24-hour period in a given area. Being able to better predict and understand these spikes (where, when, and why they occur) would allow healthcare officials to better determine when and how to allocate resources to mitigate and prevent future spikes. Along with healthcare professionals, our analysis could help doctors and hospitals better prepare for an increased number of patients as well as legislators and detect how susceptible their community is to potential Covid spikes. 
Objectives:

**Our methodology can be broken down into the following components:**

1. **Data collection** → Using the Northwestern library as well as other databases (Kaggle, Google Datasets, etc.) gather historical data on Covid-19 cases, deaths, and relevant features. Sources include official health department records, Census data, CDC data, and other reputable databases. Further, Collect data on potential predictors, such as population density, vaccination rates, testing infrastructure, socio-economic factors, and environmental conditions.

2. **Data processing** → Using python, Clean and preprocess the data to handle missing values, outliers, and inconsistencies. Normalize or standardize numerical features if necessary and code categorical variables appropriately.

3. **Feature Selection** → Identify the most relevant features by using statistical methods or machine learning techniques (e.g., RFE, Tree-Based models, etc.) 

4. **Model Development** → Choose and create time-series models. Our Time-Series model will aim to utilize advanced techniques (e.g., random forest, gradient boosting, XGBoost, Cat Boost, etc.). Then we will continually assess the models’ performances using appropriate metrics (e.g., Mean Squared Error, R-squared, etc.) on the testing set. We will iterate on the model, fine-tuning parameters or trying different algorithms if needed.

5. **Visualization** → Create graphs and a Dashboard that maps predicted and actual Covid cases and deaths in a given county over time. Visualize the identified spikes to facilitate further analysis.]

6. **Conclusions** → Discuss the predictors contributing significantly to Covid spikes. Examine the feasibility of manipulating and tracking these features to allow healthcare decision-makers better foresight and control in the future.

7. **Documentation and Reproducibility** → Document our methodology, key findings, and any limitations. Prepare a comprehensive report or presentation for healthcare professionals, decision-makers, and other stakeholders. Validate our model using additional datasets if available. Ensure that our analysis is reproducible by documenting code and workflows.

**Final Dataset**
  - Sources: Kaggle, CDC, New York Times, BEA, Google 
  - Dimensions: 7900 rows, 51 features, 0 Missing values --> 10 states
  - Description: Each row represents a unique state and date combination and includes relevant demographic, epidemiological, economic, and other information on the additional Covid-19 cases and deaths in that state on that day 
  - Key Features: county, date, new cases, new deaths, gdp, personal income, vaccine info

**Datasets used Throughout Process**

COVID-19 Case Surveillance Public Use Data with Geography
Source: CDC → Transitioning to New York Times as we expand our data from only 2020 to 2020-2022
Dimensions: 38.5k rows by 109 columns
Description: Each row represents a positive case and includes relevant information on the patient (age, race, etc.) as well as the test (location, date, etc.)
Key Features: case month, home state and county, age, ethnicity, if the patient was hospitalized, underlying health conditions, etc.
Notes: This data is on the month level rather than the day level, which makes it difficult to use with the rest of our data

COVID-19 Vaccinations in the United States, County
Source: CDC 
Dimensions: 104M rows by 19 columns
Description: Each row includes information about the vaccine status for a given county and day
Key Features: date, county, vaccine rate per 100,000 people of different age and ethnic groups in the given jurisdiction, breakdown of which vaccines were administered, etc.
Notes: This data is on the state level rather than the county level making it difficult to merge with county data
United States COVID-19 Community Levels by County

Source: CDC 
Dimensions: 206k rows by 12 columns
Description: Each row represents a county and includes relevant information on demographics and Covid-19 statistics
Key Features: county, population, health service area population, Covid-19 community level
Notes: This data does not include information on the demographics of each county

Kaggle Dataset: Covid_by_county.csv
Source: Kaggle 
Dimensions: 360k rows by 6 columns
Description: Each row represents a unique county and date combination and includes relevant information on the additional Covid-19 cases and deaths in that county on that day 
Key Features: county, date, new cases, new deaths

Annual County Resident Population Estimates by Demographic
Source: Census.gov 
Dimensions: 239k rows by 80 columns
Description: Each row represents a unique county and age group in each year from 2020 to 2022 and includes detailed information on population demographics in each location
Key Features: county, breakdown by race, gender

Annual County Resident Population Estimates by Age Group
Source: Census.gov 
Dimensions: 12.5k rows by 96 columns
Description: Each row represents a unique county in each year from 2020 to 2022 and includes detailed information on population in each age group
Key Features: county, age breakdown

Annual County GDP Data
Source: Bureau of Economic Analysis
Dimensions: 31k rows by 7 columns
Description: Each row represents a unique county and descriptor and includes data on each given descriptor (GDP with 2017 base, GDP in current year, etc.) in each year from 2020 to 2022
Key Features: county, year, GDP data

Annual County Personal Income Data
Source: Bureau of Economic Analysis
Dimensions: 31k rows by 7 columns
Description: Each row represents a unique county and descriptor (personal income, population, etc.) and includes data on each given descriptor in each year from 2020 to 2022
Key Features: county, year, personal income data
