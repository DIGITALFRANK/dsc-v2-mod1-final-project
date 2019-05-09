
# King County, Oregon (Seattle Area) House Sale Data Multivariable Linear Regression & OLS


## Introduction

In this project we analyzed home sale data from King County, Oregon (Seattle area) between 2014-2015
Based on our findings in the dataset, we engineered some new features and implemented Multivariate Linear Regression to most accurately predict our target of Sale Price


## Objectives
Our goal was to:
* Access data and transform it into the most desireable format
* work with clean, consistant, and meaningful data 
* implement Multiple Regression and Ordinary Least Squares
* Find the most accurate function to predict Sale Price of a home in King County



## The Dataset

For this project, we be worked with the King County House Sales dataset.  The dataset can be found in the file `"kc_house_data.csv"`, in this repo. 

As the column names and their descriptions were not perfectly described, we did do some additional research and used our best judgment relating to what the data actually means.  Overall, things were pretty clear and we quickly gathered an idea of which features we would use and which we would disguard or ignore.

A sample of the original data...

![raw_data_sample](https://raw.githubusercontent.com/DIGITALFRANK/dsc-v2-mod1-final-project/master/raw_data_sample.png)




## The Deliverables

There will be four  deliverables for this project:


## The Process

### 1. Getting Started

start of `presentation.pdf`.

### 2. The Project Review

> **When you start on the project, please also reach out to an instructor immediately to schedule your project review** (if you're not sure who to schedule with, please ask in slack!)

#### What to expect from the Project Review



#### 1. Deliver your PDF presentation to a non-technical stakeholder. 


#### 2. Go through the Jupyter Notebook, answering questions about how you made certain decisions. Be ready to explain things like:
    * "how did you pick the question(s) that you did?"
    * "why are these questions important from a business perspective?"
    * "how did you decide on the data cleaning options you performed?"
    * "why did you choose a given method or library?"
    * "why did you select those visualizations and what did you learn from each of them?"
    * "why did you pick those features as predictors?"
    * "how would you interpret the results?"
    * "how confident are you in the predictive quality of the results?"
    * "what are some of the things that could cause the results to be wrong?"

Think of the first phase of the review (~30 mins) as a technical boss reviewing your work and asking questions about it before green-lighting you to present to the business team. You should practice using the appropriate technical vocabulary to explain yourself. Don't be surprised if the instructor jumps around or sometimes cuts you off - there is a lot of ground to cover, so that may happen.

If any requirements are missing or if significant gaps in understanding are uncovered, be prepared to do one or all of the following:
* Perform additional data cleanup, visualization, feature selection, modeling and/or model validation
* Submit an improved version
* Meet again for another Project Review

What won't happen:
* You won't be yelled at, belittled, or scolded
* You won't be put on the spot without support
* There's nothing you can do to instantly fail or blow it

**Please note: We need to receive the URL of your repository at least 24 hours before and please have the project finished at least 3 hours before your review so we can look at your materials in advance.** 


## Requirements

This section outlines the rubric we'll use to evaluate your project.

### 1. Technical Report Must-Haves

For this project, your Jupyter Notebook should meet the following specifications:

#### Organization/Code Cleanliness

* The notebook should be well organized, easy to follow,  and code should be commented where appropriate.  
    * Level Up: The notebook contains well-formatted, professional looking markdown cells explaining any substantial code.  All functions have docstrings that act as professional-quality documentation
* The notebook is written for technical audiences with a way to both understand your approach and reproduce your results. The target audience for this deliverable is other data scientists looking to validate your findings. 

#### Visualizations & EDA

* Your project contains at least 4 meaningful data visualizations, with corresponding interpretations. All visualizations are well labeled with axes labels, a title, and a legend (when appropriate)  
* You pose at least 3 meaningful questions and answer them through EDA.  These questions should be well labeled and easy to identify inside the notebook. 
    * **Level Up**: Each question is clearly answered with a visualization that makes the answer easy to understand.   
* Your notebook should contain 1 - 2 paragraphs briefly explaining your approach to this project.
    
#### Model Quality/Approach

* Your model should not include any predictors with p-values greater than .05.  
* Your notebook shows an iterative approach to modeling, and details the parameters and results of the model at each iteration.  
    * **Level Up**: Whenever necessary, you briefly explain the changes made from one iteration to the next, and why you made these choices.  
* You provide at least 1 paragraph explaining your final model.   
* You pick at least 3 coefficients from your final model and explain their impact on the price of a house in this dataset.   


### 2. Non-Technical Presentation Must-Haves

Your presentation should:

* Contain between 5 - 10 professional-quality slides.  
    * **Level Up**: The slides should use visualizations whenever possible, and avoid walls of text. 
* Take no more than 5 minutes to present.   
* Avoid technical jargon and explain the results in a clear, actionable way for non-technical audiences.   

**_Based on the results of your models, your presentation should discuss at least two concrete features that highly influence housing prices._**

### 3. Blog Post


## Submitting your Project



## Summary

By engineering a 'price_per_sqft_living' feature, we were able to pass in the best possible independent variables to our Multivariate Regression model, which returned a confidant R^2 value of **0.881**.  We will continue our process by logging Sales Data for an even stronger model, followed by training and testing our model against the dataset for best results.

By examining our model's coefficients, we conluded that a home's sale price in King County can be predicted with the following formula:

y = (6.5 * 10^3) + 297.4770**x1** + 2089.6125**x2** + 9811.1640**x3**

where x1, x2, and x3 represent the home's **square footage of living space**, **price per square foot of living space**, and **number of bathrooms**, respectively.  Please See the presentation PDF in this repo for a quick summary of our process and findings



