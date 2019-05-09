
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

Think of the first phase of the review (~30 mins) as a technical boss reviewing your work and asking questions about it before green-lighting you to present to the business team. You should practice using the appropriate technical vocabulary to explain yourself. Don't be surprised if the instructor jumps around or sometimes cuts you off - there is a lot of ground to cover, so that may happen.

If any requirements are missing or if significant gaps in understanding are uncovered, be prepared to do one or all of the following:
* Perform additional data cleanup, visualization, feature selection, modeling and/or model validation
* Submit an improved version
* Meet again for another Project Review


### 3. Prediction Approach



* The notebook should be well organized, easy to follow,  and code should be commented where appropriate.  
    * Level Up: The notebook contains well-formatted, professional looking markdown cells explaining any substantial code.  All functions have docstrings that act as professional-quality documentation
* The notebook is written for technical audiences with a way to both understand your approach and reproduce your results. The target audience for this deliverable is other data scientists looking to validate your findings. 



### 3. Model Implementation

* Your project contains at least 4 meaningful data visualizations, with corresponding interpretations. All visualizations are well labeled with axes labels, a title, and a legend (when appropriate)  
* You pose at least 3 meaningful questions and answer them through EDA.  These questions should be well labeled and easy to identify inside the notebook. 
    * **Level Up**: Each question is clearly answered with a visualization that makes the answer easy to understand.   
* Your notebook should contain 1 - 2 paragraphs briefly explaining your approach to this project.
      




## Our Results


### A Multivariable Regression model using square foot of living space and price per square foot of living space is a good predictor of Sale Price 

Your presentation should:

* Contain between 5 - 10 professional-quality slides.  
    * **Level Up**: The slides should use visualizations whenever possible, and avoid walls of text. 
* Take no more than 5 minutes to present.   
* Avoid technical jargon and explain the results in a clear, actionable way for non-technical audiences.   

**_Based on the results of your models, your presentation should discuss at least two concrete features that highly influence housing prices._**




## Summary

By engineering a 'price_per_sqft_living' feature, we were able to pass in the best possible independent variables to our Multivariate Regression model, which returned a confidant R^2 value of **0.881**.  We will continue our process by logging Sales Data for an even stronger model, followed by training and testing our model against the dataset for best results.

By examining our model's coefficients, we conluded that a home's sale price in King County can be predicted with the following formula:

y = (6.5 * 10^3) + 297.4770**x1** + 2089.6125**x2** + 9811.1640**x3**

where x1, x2, and x3 represent the home's **square footage of living space**, **price per square foot of living space**, and **number of bathrooms**, respectively.  Please See the presentation PDF in this repo for a quick summary of our process and findings



