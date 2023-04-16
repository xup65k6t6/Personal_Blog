---
layout: page
title: "Kaggle: Spaceship Titanic"
tags: [about, Jekyll, theme, moon]
date: 2023-04-15
comments: false
---


# Introduction

This is a kaggle competition to predict which passengers are transported to an alternate dimension. 
The data source is from [https://www.kaggle.com/competitions/spaceship-titanic](https://www.kaggle.com/competitions/spaceship-titanic)

I blended predictive results using Vote Classfifier from three different model --  CatBoost, XGBoost, and LGBM -- to maximize accuracy of the prediction.

\\ start from here

# Datasets
* 12 variables for each passenger and a column for succesfully transported or not (y variable). Total 8,693 rows.
* After data cleaning, I kept all rows and imputed missing values.


# Language and libraries
**Language** : Python

**Libraries** : 
* Data Manipulation: pandas, numpy
* Data Visualization: matplotlib, seaborn
* Machine Learning: sklearn, xgboost, lightgbm, catboost


# Data Preprocessing
## Impute missing values

* **Insights** : 



# Feature Engineering


# EDA (Exploratory Data Analysis) and Feature Selection
* Visualize correlation between all features


* Visualize correlation after removing high correlation (>= 0.85) & check pairplot

* Add categorical variable Recent_Trend and draw a heatmap again



# Model Build-up
* Split Data: 80.1% training set, 9.9 validation set, 10% test set

* Pipeline
 * Feature pipeline: use pipeline to connect data preprocessing among different features
  * Drop features
  * Numerical features: simple impute to median (although we have done this by hand before)
  * Special numerical feature: for the All-Poverty feature, I noticed it would be better to do a log transformation
  * Categorical features: simple impute to most frequent value, and do one-hot encoding
 * Model pipeline: After building up feature pipelines, I connected them to the model or algorithms, so I don't need to do the same task again on test data set.


# Model Selection
## Linear Regression
* Simple Linear Regression
* Ridge Regression
* Lasso Regression

## Non-linear Algorithms
* Random Forest
* XGB Regressor


# Evaluation
* MSE
* R-squared
* MAE


# Potential future improvement
- Semi-supervised learning: when imputing the missing value, doing semi-supervised learning may be helpful. It can prevent from losing information (remove missing value rows) and still relatively maintain the accuracy.
- Correctly tung hyperparameter: when tuning hyperparameter in XGBoost, I accidently guess the best parameters and did not put a wider range into searching CV loop. So, it is possible to have a higher score if I tune the hyperparameters correctly.

# Takeaways
- Clean dirty and missing data from the scratch
- Use pipeline to connect every step from imputing to training models
- Tune hyperparameter
- Deploy Ridge, Lasso, Random Forest, and XGBoost algorithms for the first time

# Code
For code detail, you can check [here](https://github.com/xup65k6t6/Lung-Cancer-Mortality-Rate-Prediction).
