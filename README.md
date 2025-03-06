# Financial-Portfolio-Construction
## Overview
This project aims to construct a financial portfolio by predicting future returns based on historical financial factors. Ridge regression was used to model the relationships between factors and future returns, and then optimize portfolio performance by selecting the best alpha (regularization parameter) for Ridge regression. The project involves several steps, including data preprocessing, regression modeling, and performance evaluation of the portfolio.

---

## Table of Contents

1. [Dataset](#dataset)
2. [Steps](#steps)
3. [Results](#results)
 
---

## Dataset
The data is provided in the CSV file factor_and_ret_oos.csv, which contains historical financial factors and future returns. The data is structured with an index of id and date, with multiple financial factors as columns.

---

## Steps 
1. **Data Preprocessing**
Load the data and clean it by removing unnecessary columns.
Split the dataset into factors and future_return variables.
Handle missing values by filling them with zeros and normalize the data.
2. **Compute Correlations**
Compute the pairwise correlations between financial factors over rolling 3-year windows at 6-month intervals.
3. **Ridge Regression Model**
Fit a Ridge regression model for different levels of the regularization parameter (alpha), using a rolling window of 3 years of historical data to predict future returns.
Perform regression for various alpha values to determine the optimal alpha based on the Sharpe ratio of the predicted portfolios.
4. **Portfolio Construction**
After predicting returns with Ridge regression, construct portfolios by allocating weights based on predicted returns.
Evaluate portfolio performance using the Sharpe ratio to identify the best performing portfolio.
5. **Performance Evaluation**
Compute both the actual and expected (unconditional) Sharpe ratios for portfolios.
Visualize the returns of portfolios with different alphas to understand the relationship between the regularization parameter and portfolio performance.


## Results
- **Best Alpha**: The best alpha for Ridge regression is determined by maximizing the Sharpe ratio. In this project, the best alpha was found to be logalpha_3.0.

- **Portfolio Performance**: The portfolio returns are evaluated and plotted for different alphas. Higher alpha values lead to a more regularized model with higher bias and lower variance, which impacts the portfolio's performance.
