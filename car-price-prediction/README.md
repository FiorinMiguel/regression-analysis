# Used Car Price Prediction — Multiple Linear Regression

Multiple linear regression model built in R to predict used car sale prices based on objective vehicle characteristics, using the public CarDekho dataset (~7,900 real listings).

![R](https://img.shields.io/badge/R-Statistical%20Analysis-blue)
![tidyverse](https://img.shields.io/badge/tidyverse-data%20wrangling-1f77b4)

![Preview](path/to/screenshot.png)

## About the project

The project covers the full analytical pipeline: data cleaning, feature engineering, exploratory analysis, and model diagnostics. The initial model showed heteroscedasticity and non-normality of residuals, addressed by applying a log transformation to the response variable, centering the predictors, and removing influential points. An interaction between horsepower and vehicle age was also included, capturing how the value gained from horsepower diminishes as the car ages.

With these adjustments, R² improved from 0.67 to 0.87, and residuals showed well-behaved patterns.

## Methodology

- **Data cleaning & feature engineering** on ~7,900 real listings from CarDekho
- **Exploratory analysis** to identify relationships between predictors and price
- **Model diagnostics:**
  - Multicollinearity checked via GVIF
  - Heteroscedasticity tested with Breusch-Pagan
  - Autocorrelation tested with Durbin-Watson
- **Log-transformed response**, allowing coefficients to be interpreted as percentage effects
- **Prediction** on three car profiles, with 95% confidence intervals

## Key findings

Since the response is on a log scale, coefficients translate directly into percentage effects:

- Each additional year of age reduces the price by **~11%**
- Manual transmission vehicles cost **~13% less** than automatics
- Horsepower's effect on value diminishes as the vehicle ages (horsepower × age interaction)

## Tools

- **Language:** R
- **Packages:** tidyverse, car, lmtest, ggplot2

![Full Project Report](Car-Price-Prediction-Report.pdf)
