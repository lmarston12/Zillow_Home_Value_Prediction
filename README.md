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
To save on memory, I explored the number of properties in my dataset that did not have a matching train record. I found that almost 3 million properties did not have corresponding target data (those properties did not sell, therefore, we do not know the sale price), so those entries were separated out. 

One thing I did during the initial analysist was to check the range for the different transaction dates and it is visualized below:

![](images/transactiondatehist)

I also found that some of the homes were sold twice during the period that the training data was captured which left multiple records for a particular parcelId. 
Because only ~100 of the ~90,000 properties had multiple records, we chose to just take a random sales record for each parcel with more than one sales record (as opposed to... always using the most recent record, always using the oldest record, using both records, or engineering a feature from the info).

When exploring Unique Values in the dataset a few things that I looked for are:
* Are any of the features all of the same value? These won't be useful in a model, so I discarded them
* Are any features discrete with high cardinality? These wouldn't hold very much information because there would only be a few records for each "level" of the categorical feature

I also found it interesting to explore the Target Variable, shown below:

![](images/targetdistribution)

I keep this in mind when choosing Machine Learning Algorithms and corresponding loss functions. When I plotted the density on a log-scale, the target looks closer to a Normal Distribution:

![](images/targetlogscale)

## Feature Engineering



## Modeling


## Results


## Next Steps


## Appendix
