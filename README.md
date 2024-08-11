# Yulu Bike Demand Analysis: Exploratory Data Analysis (EDA)

## Overview

Yulu is India's leading micro-mobility service provider, offering unique electric vehicles for daily commutes. With a mission to eliminate traffic congestion, Yulu provides a safe and user-friendly commuting solution through a mobile app, enabling shared, solo, and sustainable commuting. Yulu zones are strategically located across metro stations, bus stands, office spaces, residential areas, and corporate offices to ensure smooth, affordable, and convenient first and last-mile connectivity.

### Project Objective

Yulu has experienced a significant dip in its revenues and has sought the help of a consulting firm to understand the factors influencing the demand for shared electric cycles in the Indian market. The primary objectives of this analysis are:

- To identify significant variables that predict the demand for shared electric cycles.
- To evaluate how well these variables describe the demand for electric cycles.

## Data Exploration

- **Dataset Information:** The dataset contains 10,885 rows and 12 columns with no null values. It covers the period from January 1, 2011, to December 19, 2012.
- **Outlier Detection:** Windspeed exhibited the most outliers, indicating the potential presence of non-normal distributions in the data.

## Univariate Analysis

- **Season:** The dataset includes four unique seasons. 
- **Holiday:** Binary classification (0: not a holiday, 1: holiday).
- **Working Day:** Binary classification (0: not a working day, 1: working day).
- **Weather:** The weather conditions range from clear to heavy rain, with clear weather having the most observations.

## Bivariate Analysis

### Hour vs. Count, Casual, and Registered

- **Peak Hours:** Most bikes are rented at 8 AM, 5 PM, and 6 PM, aligning with typical office hours.
- **Casual Rentals:** Casual bike rentals peak between 12 PM and 5 PM.
- **Registered Rentals:** Registered bike rentals peak at 8 AM, 5 PM, and 6 PM, indicating a strong connection to office commutes.

## Hypothesis Testing

### Working Day vs. Count

- **Null Hypothesis (H0):** The mean count on working days equals the mean count on non-working days.
- **Result:** The p-value from the two-sample t-test is greater than 0.05, indicating no significant difference between the mean counts on working and non-working days.

### Weather vs. Count

- **Null Hypothesis (H0):** Mean ride counts are the same for clear, mist, and light rain weather.
- **Result:** Kruskal-Wallis test results in a p-value less than 0.05, indicating a significant difference in ride counts between at least one pair of weather conditions.

### Chi-Square Test: Weather and Season

- **Null Hypothesis (H0):** Season does not impact weather.
- **Result:** The p-value is less than 0.05, suggesting that the season does impact weather conditions.

## Correlation Analysis

- **Temperature:** Weak positive correlation with ride counts.
- **Humidity:** Weak negative correlation with ride counts.
- **Windspeed:** No significant correlation with ride counts.

## Conclusion

Based on the EDA:

- **Weather conditions** play a significant role in determining ride counts, with clear skies and misty weather conditions leading to higher demand.
- **Seasonal changes** affect weather patterns, indirectly impacting ride counts.
- **Operational Recommendations:** Consider adjusting the number of bikes and operational costs during rainy or snowy seasons to optimize resource allocation.

## Google Colab Notebook

For a detailed walkthrough of the analysis, please refer to the Google Colab notebook:

[Yulu EDA Notebook](https://colab.research.google.com/drive/1ZDy7ioM658qemJU3qtNTajtUJElzKX-f?usp=sharing)

