# Applied-Statistics-Predicting-Solar-Radiation

Project Overview

This project investigates the statistical relationship between Daily Maximum Temperature (X) and Daily Total Solar Radiation (Y) in London. Using a year of historical data (n=365), the study explores joint distributions, tests for linear dependence, and validates the assumptions of Ordinary Least Squares (OLS) regression through residual analysis.

The core goal is to demonstrate a rigorous statistical workflow—from data retrieval via API to formal hypothesis testing and checking the properties of marginal and joint distributions.

Tech Stack:
Language: Python 3.x
Libraries: pandas, numpy, scipy.stats, matplotlib, seaborn
Data Source: Open-Meteo Historical Weather API

Methodology & Key Tasks:
1. Data Retrieval & Exploratory Analysis
Programmatic data fetching using the Open-Meteo API.
Generation of descriptive statistics and 2D scatter plots to visualize the empirical joint distribution.

2. Linear Dependence Testing
Method: Pearson Correlation Coefficient (r) and Student’s t-test.
Hypothesis: H0:ρ=0 vs H1:ρ=0.Visuals: Theoretical PDF of the t-distribution with shaded critical regions and p-value areas.

3. OLS Regression & Residual Analysis
Implementation of a linear model: Y=aX+b+ϵ.
Normality Testing: Used the Kolmogorov-Smirnov (KS) Test to verify if residuals ϵ follow a Gaussian distribution N(0,s2).
Result: Failed to reject H0 at α=0.05 (p≈0.093), validating the linear model assumptions.

4. Independence via Marginals
Theoretical exploration of the factorization property: P X,Y=PX⊗PY.
Proposed a 2D contingency table and Chi-squared test approach to evaluate whether the variables are stochastically independent beyond simple correlation.

Key Findings
Strong Correlation: A significant positive linear relationship was identified between temperature and solar radiation (r≈0.82).

Model Fit: The OLS model effectively captures the trend, with residuals that plausibly represent white noise.

Physical Insight: The "shared randomness" is attributed to atmospheric systems where clear skies simultaneously drive high radiation and surface heating.

How to Run
Clone the repository.

Ensure you have the required libraries: pip install pandas scipy matplotlib seaborn requests.

Open the Jupyter Notebook Applied_Stats_CW2.ipynb and run all cells.
