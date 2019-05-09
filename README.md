
# King County, Oregon (Seattle Area) House Sale Data Multivariable Linear Regression & OLS


## Introduction

In this project we analyzed home sale data from King County, Oregon (Seattle area) between 2014-2015.  
Based on our findings in the dataset, we engineered some new features and implemented Multivariate Linear Regression to most accurately predict our target of Sale Price


## Objectives
Our goal was to:
* Access data and transform it into the most desireable format
* work with clean, consistant, and meaningful data 
* implement Multiple Regression and Ordinary Least Squares
* Find the most accurate function to predict Sale Price of a home in King County



## The Dataset

For this project, we worked with the King County House Sales dataset.  The dataset can be found in the file `"kc_house_data.csv"`, in this repo. 

As the column names and their descriptions were not perfectly described, we did do some additional research and used our best judgment relating to what the data actually means.  Overall, things were pretty clear and we quickly gathered an idea of which features we would use and which we would disguard or ignore.

A sample of the original data...

![raw_data_sample](https://raw.githubusercontent.com/DIGITALFRANK/dsc-v2-mod1-final-project/master/raw_data_sample.png)




## Homes Sale Price Distribution

Our predition target, 'price' in its distribution:

![raw_data_sample](https://raw.githubusercontent.com/DIGITALFRANK/dsc-v2-mod1-final-project/master/price_dist.png)


Though Sale Price distribution was skewed right, we felt no need to normalize at this instant because we believed the outliers to be **TRUE**, as in a clear and constant linear repesentation of price, as related to other variables


## The Process

### 1. Getting Started

We start with some initial Exploratary Data Analysis on the raw data set and see how the different features relate to our prediction target `price`.

### 2. Finding Substance

> **We want to find the features, or independent variables, whose correlation with the prediction target is most significant** (after cleaning/munging/wrangling and formating our data as necessary, we start to see these relationships more clearly)


#### We got the following insights from out data:

    * Square foot of living space had the hightst correlation with Sale Price
    
    * Home values differ drastically depending on location (ask any real estate agent!)
    
    * The bedroom to bathroom ratio and their amounts can tell a good story about Sale Price
    
    * How old the house is doesn't not seem to have a major impact on Sale Price
    
    * Home Condition & Grade are consistant with Sale Price
    
    * Sale Price increases as Latitude and Longitude approaches the city of Seattle
    
    * Whether the home has been viewed and how many times by real estate agents has no impact on Sale Price 
    
    * A large basement can be an asset to a home's Sales Price but is not a predictor of Sale Price
    
    * (reported) Renovation does not seem to greatly impact Sale Price

Our model will only be good as the data we feed it.  It is very important that not only does it make common sense to predict from this data, but also that the data is rich in its amount and direct correlation to our prediction target.  Some categorical data, such as the zipcode of homes seem very attractive at this point, however, feeding our linear model a bunch of zipcodes does nothing in evaluating the relationship between a home's sales price and its zipcode (our model is linear).  One option would be to somehow wrangle zipcodes and latitudes and longitudes together to find some kind of linear value of location, but clearly that would be using a wrench to stab a pin, and it offers us no guarantee.



### 3. Prediction Approach

After careful consideration, we decided that using the highest correlated variable, `sqft_living`, or square foot of living space to feed our model was our best route.  Additionally, to account for location pricing in a clever and yet linear fashion, we engineered a new feature`price_per_sqft_living` which takes a home's total square foot of living space and divides it by its sale price.  This new feature indireclty accounts for location pricing as homes in a general area have a similar price per sqare foot, it remains linear which is good food for our Regression model.  It also uses past sales price data to predict future sales prices, which is what is most common sense.  For our Multivariate Linear Regression model, we also added `bathrooms`, the number of bathrooms the home has, as an independent variable predictor.  This variable is a good indicator of the home's size and numbe of bedrooms, ie: living space the home has.  



### 3. Model Implementation

blah blah blah
      




## Our Results


### A Multivariable Regression model using square foot of living space and price per square foot of living space is a good predictor of Sale Price 

blah blah blah

 

**_Based on the results of your models, square foot of living space and price per square foot are the strongest predictors of a home's Sale Price.  Bathrooms also add value to homes and is a good predictor to consider_**




## Summary

By engineering a 'price_per_sqft_living' feature, we were able to pass in the best possible independent variables to our Multivariate Regression model, which returned a confidant R^2 value of **0.881**.  We will continue our process by logging Sales Data for an even stronger model, followed by training and testing our model against the dataset for best results.

By examining our model's coefficients, we conluded that a home's sale price in King County can be predicted with the following formula:

y = (6.5 * 10^3) + 297.4770**x1** + 2089.6125**x2** + 9811.1640**x3**

where x1, x2, and x3 represent the home's **square footage of living space**, **price per square foot of living space**, and **number of bathrooms**, respectively.  Please See the presentation PDF in this repo for a quick summary of our process and findings



