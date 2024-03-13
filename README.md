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
