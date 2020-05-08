# Zillow_Home_Value_Prediction
Predicting the log-error between 'Zestimate' and actual home value

## Introduction
This project aims to predict the log(error) of Zillow’s estimate ('Zestimate') and the actual sale prices in California for a specified number of months in 2016 and 2017. According to the National Association of Realtors, more than 5 million units of existing homes were sold in the US in 2020. Home purchase signifies a significant expense for any individual, therefore, a lot of research goes into buying a home. Home price estimates would give the seller and the buyer a reference point, which would thus reduce the time and effort of both parities involved. As a result, a good home price estimate would reduce a lot of unnecessary cost, and would help both the buyers and sellers.

In this project, I use the dataset provided by Zillow for a Kaggle competition, and apply linear and gradient boosting regression to predict the log(error) of Zillow’s estimate. I use the Mean Absolute Error to evaluate the model as it is mathematically easy to define and we can figure out the difference in the price error of the estimate.

![](images/ZillowKaggle.jpg)

## Data
The data for this project comes from Zillow for a Kaggle competition. The dataset 60 features that described the location, year built, square footage, number of bedrooms and bathrooms, tax amount, among many others. The model aims to predict the log(error), which is described as:

logerror = log(Zestimate) - log(SalePrice)

## Exploratory Data Analysis
