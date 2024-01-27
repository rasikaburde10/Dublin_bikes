# Dublin_bikes

# Project Overview
This project utilizes machine learning to estimate the potential usage of city bikes in a hypothetical scenario where the COVID-19 pandemic did not occur. By analyzing historical bike usage data, the project aims to understand the pandemic's impact on urban mobility and provide insights into city bike service optimization.

# Data Pre-Processing and Feature Engineering

**Data Collection**


Dataset Source: The dataset was obtained from the Dublin Bikes API, covering the period from August 1, 2018, to December 23, 2023.


Data Consolidation: Data, available in quarterly and monthly formats, was merged annually for ease of analysis.


**Categorization**


Time Periods: The dataset was divided into pre-pandemic (Aug 2018-Dec 2019), pandemic (Jan 2020-Mar 2022), and post-pandemic (Apr 2022-Dec 2023) categories.
Data Enhancement


Weather Data: Additional weather data (tempmax, tempmin, percip, humidity) from Visual Crossing was integrated.


Data Transformation: The 'TIME' column was split into 'DATE' and 'TIME_ONLY', enriching the dataset structure.


**Exploratory Data Analysis (EDA)**


Correlation Analysis: Initial EDA focused on understanding data trends and identifying key features like bike stands, available bikes, and station ID.


Weather Impact: EDA included scatter plots and Pearson correlation coefficients to assess weather's influence on bike usage.


**Feature Selection**


Key Features: Based on EDA, significant features such as 'total usage', 'bikes in', 'bikes out', and 'interval' were selected for their impact on bike-sharing trends.


# Machine Learning Model


Model 1: Ridge Regression


Data Preparation: Separate preparation of pre-pandemic and pandemic datasets.


Feature Engineering: Creation of lagged features for time series forecasting.


Model Training and Evaluation: Training with cross-validation and performance metrics analysis.


Model 2: LSTM


Data Preparation and Scaling: Normalization of data using MinMaxScaler.


Model Architecture: Construction of a Sequential LSTM model with Dropout and Dense layers.


Forecasting and Inverse Scaling: Predictions for bike rentals during the COVID period and conversion back to original scale.


# Evaluation and Insights


Ridge Regression:

Visual and statistical performance analysis.

RMSE, MAE, and R-squared value assessment.

Cross-validation insights.


LSTM:

RMSE, R-squared, and MAE evaluation.


Comparative assessment with Ridge Regression.


Visual match and overall performance assessment.


# Conclusion


The project provides a nuanced understanding of city-bike usage patterns and highlights the significant impact of the COVID-19 pandemic on urban mobility. The LSTM model, in particular, showcases the potential of machine learning in adapting to complex, real-world scenarios, offering valuable insights for future urban planning and transportation strategies.
