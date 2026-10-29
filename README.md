# us-depression-analysis

## Overview
Statistical analysis focusing on depression rate in the U.S. Least squares regression was run on other chronic disease indicators to measure level of influence from obesity, poverty, sleeplessness, inactivity, and regular checkups on depression on a state by state level.

## Data
CDC U.S. Chronic Disease Indicators (2019-2023)
The regression uses 2022 data for the 50 states.
https://catalog.data.gov/dataset/u-s-chronic-disease-indicators

## Tools
- Python (pandas, matplotlib, seaborn, statsmodels)
- Tableau Public

## Files
- python chronic disease.ipynb is the notebook with output, code, and notes.
- state_data_2022.csv is the cleaned dataset for regression analysis.
- Link to Tableau Dashboard showing depression by state (https://public.tableau.com/app/profile/benjamin.frink/viz/StatebystateDepression/Dashboard1)
- Link to Tableau Dashboard showing nationwide depression stats (https://public.tableau.com/app/profile/benjamin.frink/viz/NationwideDepressionRates/NationwideDepressionRates)

## Key Findings
- Together, the five predictors explain about 25% of the variation in depression between states in 2022 (adj. R² = 0.25, F-test p = 0.003).
- Obesity (β = 0.51, p = 0.004) and poverty (β = 0.48, p = 0.018) are statistically significant positive predictors of depression on a state by state level in 2022.
- Checkup rates and sleeplessness are not statistically significant predictors.
- On a nationwide level depression rate in 2022 varied drastically by sex (Male = 15.2 Female = 26.9) and race (Asian non-Hispanic = 9.9 Multiracial non-Hispanic = 30.6).
- Model diagnostics support regression assumptions. Results were consistent when most influential states were removed.

## Limitations
- The depression measure counts adults ever told by a health professional that they have depression. So, states that have less care access may show lower results than actual rates.
- Poverty uses crude prevalence while other measures are age-adjusted.
- Results show inactivity is a significant negative predictor of depression. This is likely due to its strong correlation with poverty (r = 0.80) and obesity (r = 0.72).
- This is an observational analysis of state and national data. It shows only correlation, not causation and it cannot be used to make estimates about individuals.
