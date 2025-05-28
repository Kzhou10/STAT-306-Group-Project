# Vehicle Price Prediction – STAT 306 Final Project

## Overview
This project investigates the key factors influencing the price of vehicles using multiple linear regression and model selection techniques. We analyzed a dataset of over 3,800 car listings scraped from YallaMotor and applied statistical modeling to determine which vehicle specifications and manufacturer origins significantly impact pricing. The project was completed as part of the STAT 306: Applied Regression Analysis course at Simon Fraser University.

## Objectives
- Identify which car features most significantly affect vehicle price.
- Build a robust linear regression model to quantify these effects.
- Use subset selection and diagnostic tools to improve model interpretability and performance.
- Provide insights for potential buyers and industry stakeholders based on statistical evidence.

## Key Findings
- Horsepower, top speed, number of cylinders, and manufacturer country were strong predictors of price.
- Cars manufactured in Germany and the UK tended to be significantly more expensive, while those from China and South Korea were generally more affordable.
- The final full model explained 88.7% of the variance in log-transformed car prices.
- Multicollinearity was not a concern (all VIFs < 10).
- A subset model using 6 predictors provided a strong trade-off between simplicity and performance.

## Methods and Tools
- **Language**: R
- **Techniques**:
  - Multiple Linear Regression (`lm()`)
  - Subset Selection (`regsubsets()`)
  - Variance Inflation Factor (VIF) for multicollinearity
  - Diagnostic Plots (Residuals, QQ Plot)
  - Data transformation (log transformation, currency conversion)
- **Packages**: `leaps`, `car`, `ggplot2`, `dplyr`

## Data Description
- **Source**: Scraped from [YallaMotor](https://www.yallamotor.com/)
- **Size**: ~3,850 cleaned entries
- **Variables**:
  - `Price (CAD)` – Response variable
  - `Engine Capacity`
  - `Number of Cylinders`
  - `Horsepower`
  - `Top Speed (km/h)`
  - `Number of Seats`
  - `Country of Manufacturer` (derived from brand)

## Model Performance

| Model                | R²     | Adjusted R² | Mallow’s Cp |
|---------------------|--------|--------------|--------------|
| Full Model           | 0.8870 | 0.8866       | 12.00        |
| Best Subset (6 vars) | 0.8794 | 0.8792       | 258.94       |

## Limitations
- Data is sourced from Middle Eastern listings, which may limit generalizability to other markets (e.g., Canada).
- Brand-level information was generalized into countries, which may reduce price precision (e.g., Ferrari vs. Fiat).
- Minor residual deviations suggest slight non-normality in upper price ranges.
- Listings may have minor inconsistencies or input errors despite filtering.

## Authors
- Kelvin Zhou  
- Louis Luo  
- Ronald Liu  

**Course**: STAT 306 — Applied Regression Analysis  
**Instructor**: Kenny Chiu  
**Date**: May 27, 2025
