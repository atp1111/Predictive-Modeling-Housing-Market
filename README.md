# Ames Housing Market: Predictive Regression Analysis

This project develops a series of linear regression models to estimate the `log(SalePrice)` of residential properties in Ames, Iowa. The goal was to build a robust model for buyers, investors, and financial institutions to objectively value real estate based on core structural and temporal factors.

## 🏗️ Technical Methodology

### 1. Model Development & Selection
I developed and compared several iterations of linear models, moving from simple bivariate relationships to complex multimodal architectures:
- **Baseline Models:** Explored the impact of `SqFt`, `Bedrooms`, and `Rooms` using Pearson and Kendall's Tau correlation.
- **Nested Model Testing:** Utilized **F-tests** to evaluate the statistical significance of interaction terms (e.g., Bedrooms * Rooms).
- **Feature Engineering:** Incorporated `log(Age)` and `log(LotArea)` to account for non-linear relationships and heteroscedasticity.

### 2. Statistical Rigor
- **Hypothesis Testing:** Performed right-tailed T-tests on coefficients to confirm positive associations between square footage and price.
- **Diagnostics:** Analyzed **Residuals vs. Fitted** and **Normal Q-Q plots** to ensure the model met standard OLS assumptions (linearity, normality, and constant variance).
- **Comparison Metrics:** Used **AIC**, **Adjusted R-squared**, and **Sigma-hat** to identify `f2` as the optimal predictive model.

## 📊 Key Findings
- **The Optimal Model:** The final model (`f2`) explained **85.3%** of the variance in sales prices by integrating structural dimensions with property age and lot size.
- **Diminishing Returns:** Discovered that while increasing bedrooms adds value in 4-room houses, the effect diminishes as the total room count increases, highlighting the importance of room-size balance.
- **Square Footage Impact:** Each additional square foot corresponds to a statistically significant **0.07%** increase in sale price, holding all other variables constant.

## 🚀 Predictive Utility
The model provides a **95% Prediction Interval** for property valuation. For example, a 2-bedroom, 1300 sq. ft. house built in 1960 on an 11,000 sq. ft. lot was predicted to sell between **$115,021** and **$196,861**, with a point estimate of **$150,476**.

## 🛠️ Tech Stack
- **Language:** R
- **Libraries:** `dplyr`, `GGally`, `ggplot2`
- **Focus:** Inferential Statistics, Linear Modeling, Data Visualization
