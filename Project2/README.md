# Project 2 - Ames Housing Data and Kaggle Challenge

Journal 1: EDA_Cleaning

## Contents:
- [Background](#Background)
- [EDA and Data Cleaning](#EDA-and-Data-Cleaning)
- [Exploratory Data Analysis Part II](#Exploratory-Data-Analysis-Part-II)
- [Pre-processing](#Pre-processing)
- [Modelling-Linear Regression](#Modelling-Linear-Regression)

--

## Problem Statement
To work on issue of under-predicting house prices via linear regression above $320,000

--

## Background 
The value of every good in a market economy is based on a price discovery process. 
Producers and resellers propose hypothetical values and hope to find buyers with similar valuations. 
In contrast, consumers bid up or push down prices based on their changing interpretations of the value of goods. 
This process is imperfect and ever-changing.<sup>1</sup> 

Hence it is crucial to come up with a one stop price prediction model to supply up-to-date insights on critical features for future sellers to add the most value to home 
--

**Citations**
<br>
<sup>1</sup> https://www.investopedia.com/ask/answers/072915/how-market-value-determined-real-estate-market.asp

--

## The Modeling Process

1. Generated two models, mainly linear regression and Lasso regression. Started off with simple linear regression without the need to penalise high coefficient variables
2. Lasso was used to incorporate most features together. 
3. Predicted price with scoring of RMSE = 19400
4. Evaluation on the models were based on mean squared error between the predicted scores vs the actual scores in the holdup test set. 
5. Models were optimised, and outliers analysed and removed to have better scoring than previous MSE. 
6. I believe the model can have more work done to improve such as 
-  Imputing rare variables 
-  Re-evaluating the use of ordinal features via EDA, either to insert ordinal numerical ranking or convert it to nominal categories
-  e-evaluate more variables that can interact better with the current interaction term via comparing correlation with sale price

--

## Significant findings

1. With the initial start, faced problem where the linear regression tends to skew upwards away from the linear predicted line 
   indicating that there is under-prediction of houses with higher sale price 
-  Hypothesise that there is some missing X-Factor that dampens the effect of grand houses as such.

2. Found that some variables do have higher correlation to price when interact with one another during the EDA. 
-  Created interaction terms between few variables. MSE improved by 18%.
-  Simulates in the real world where features are not entirely independent, as such, invoke collinearity between them. 
-  Hence, these features interact with one another to give a bigger impact to how much the house actually is worth. 

3. Optimised conversion of ordinal features into model and reduce number of features needed for Lasso regression. 
 
