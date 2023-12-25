# UpGrad - Advanced Regression - Regularization Assignment

### Problem Statement
A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

The company wants to know:

- Which variables are significant in predicting the price of a house, and
- How well those variables describe the price of a house.

Also, **determine the optimal value of lambda for ridge and lasso regression**.

## Table of Contents
* [Dataset Overview](#dataset-overview)
* [EDA Analysis](#data-analysis)
* [Model Buidling & Evaluation](#model-buidling--evaluation)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## Dataset Overview

The Australian housing market dataset has 79 features. Which includes both numerical, categorical (ordinal and nominal features).

One hot encoding of categorical features expands features to 230+

### Data Analysis

The multivariate analysis on numerical features indicates few features are  


## Model Buidling & Evaluation

The dataset has been fit to Sklearn's Linear Regression model, the evaluation results indicates high variance on test dataset. This indicates model overfitted to of train dataset.

To regularize the model, Lasso & Ridge regression is applied. The results indicates stable R2 Score.

## Conclusions

Multivariate linear regression on dataset indicates signs of multicollinearity – i.e. many predictor variables are highly correlated to each other.

This is causing the coefficient estimates of the model to be unreliable and have high variance. When the model is applied on unseen data, it is performing poorly. 

After applying ridge regression and lasso regression, we noted high ALPHA value. The shrinkage penalty (λ) approaches infinity, the shrinkage penalty becomes more influential and the predictor variables that aren’t important in the model shrink towards zero. 

### Ridge vs. Lasso Regression 

After performing k-fold cross-validation, we choose model that produces the lowest test mean squared error. In this case, Lasso Regression has lowest MSE error.

Lasso regression tends to perform better here as small number of predictor variables are significant, it’s able to shrink insignificant variables completely to zero and remove them from the model. 

## Technologies Used

The model has been built as `Jupyter Notebook` using python. It uses following Python libraries,
- numpy
- pandas
- matplotlib
- scikit-learn
- seaborn
- statsmodels
- jinja2

## Acknowledgements
- Stackoverflow
- Scikit-Learn
- Upgrade Material

## Contact
Created by [@venkataravuri] - feel free to contact me!

