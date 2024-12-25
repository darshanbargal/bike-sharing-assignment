# UpGrad: Bike-Sharing System

BoomBikes, a US-based bike-sharing service, experienced a significant revenue drop due to the Covid-19 pandemic. To prepare for post-lockdown demand, they’ve contracted a consulting firm to analyze factors affecting bike rental demand. The goal is to identify key predictors and understand their impact on demand, using an extensive dataset on daily bike usage trends and related factors. This insight will help BoomBikes position itself effectively in a recovering market and enhance profitability.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information
BoomBikes, a US bike-sharing provider, is facing significant revenue declines due to the ongoing COVID-19 pandemic. To prepare for recovery, the company is developing a strategic business plan to understand the demand for shared bikes post-lockdown. They aim to identify key factors influencing bike demand in the American market to differentiate themselves from competitors and boost profits. A consulting firm has been hired to analyze a comprehensive dataset on daily bike usage, focusing on significant variables that affect bike demand and how well these factors can predict usage trends.

### Business Problem
The goal is to model the demand for shared bikes using available independent variables, enabling management to understand how demand varies with different features. This insight will help the company adjust its business strategy to align with customer expectations and better grasp the demand dynamics in new markets.

### Data Preparation
In preparing the data, certain columns like 'weathersit' and 'season' use numeric codes (e.g., 1, 2, 3, 4) to represent categories, but these lack an inherent order. Therefore, converting them to categorical strings is recommended for clarity. The column 'yr' represents years 2018 (0) and 2019 (1). While it has only two values, it may indicate a trend of increasing demand over time, suggesting its potential relevance in predicting bike demand.

### Conclusion
**Model Equation:**
cnt = 4484.45 + 982.72 yr + 190.25 workingday + 877.36 temp - 204.61 hum - 183.56 windspeed - 526.60 spring + 271.72 winter - 162.92 July - 151.28 November + 137.03 September + 163.73 Saturday - 293.20 Light Snow - Rain & Thunderstorm - 204.03 Mist & Cloudy

**Model Evaluation:**
The close alignment of R² and Adjusted R² values between the training and test sets (R²: 0.840 vs. 0.820 and Adjusted R²: 0.840 vs. 0.820) indicates effective generalization in the linear regression model. This similarity demonstrates that the model effectively avoids overfitting to the training data, suggesting a strong potential for consistent performance on new, unseen data.

**Influential Features:**
Bike demand is influenced by various features, including year (yr), working day (workingday), temperature (temp), humidity (hum), wind speed (windspeed), and seasonal indicators such as Summer, Winter, September, and Sunday.

**Key Coefficients:**
Among the independent variables, temperature (temp), year (yr), and Winter show the highest coefficient values, highlighting their significant impact on bike demand.

**Model Fit:**
The RMSE values of 771.22 for the training set and 799.53 for the test set indicate that the model fits the training data well while generalizing reasonably to new data, as evidenced by the minimal difference between training and test set performance.

## Technologies Used
- **Python** - Version 3.17
- **Pandas** - Version 2.1.4
- **NumPy** - Version 1.26.4
- **Matplotlib** - Version 3.8.0
- **Seaborn** - Version 0.13.2
- **Jupyter Notebook** - Version 7.0.8
- **Sklearn** - Version 1.5.2
- **Statsmodels** - Version 0.14.4

## Acknowledgements
- **Data Source**: The day.csv dataset provided for this analysis from UpGrad.
- **Educational Resources**: Various online resources and courses that helped in learning EDA, Linear Regression.

## Contact
Created by [@Darshan Bargal]
