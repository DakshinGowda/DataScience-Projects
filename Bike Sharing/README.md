# Bike Sharing System

## Introduction
In this notebook, we will conduct exploratory data analysis using Pandas and Seaborn to find any relationships between Count of shared bikes and factors affecting them. This work uses Machine Learning Models to predict Count of shared bikes in a bike sharing system.

<details>
  <summary><strong>Factors that could potentially impact `Bike count` </strong></summary>
  
- `Measures` that could influence `Cnt`
  - atemp: r = 0.63
  - year: r = 0.57
  - spring: r = -0.56
  - mist cloudy: r = -0.17
  - light snow/rain: r = -0.24
  - windspeed: r = -0.24

- `Dimensions` that could influence `Cnt`
  - Season: Fall season shares highest count. Approx.500 customers prefer to take rental bikes in every season(omiting the extreme cases in winter season).
  - weathersit & Weekend: `Thusday` rentals are high. `clear` weather on weekends have high chance to rentals and ranging from 2000 to 8000 per year.
</details>


## Problem Statetment
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free.

A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. 
In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. 
They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. 
The company wants to know:
  - Which variables are significant in predicting the demand for shared bikes.
  - How well those variables describe the bike demands


## Business Goal
You are required to model the demand for shared bikes with the available independent variables. 
It will be used by the management to understand how exactly the demands vary with different features. 
They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. 
Further, the model will be a good way for management to understand the demand dynamics of a new market.


## Approach
I handled missing values in our data and split the data into training and testing datsets. Implemented feature selection technique on training dataset to enhance the performance of the model by selecting 15 most important features that impacts the target variable among 28 features(temp, winter, year,etc..). Carried out data normalization steps to fit our data to run a machine learning model like linear regression algorithm. To quantify our models I used the metrics of model accuracy. Later, Residual analysis over the final model to evaluate the goodness of a fitted model.

#### _Tools: Numpy, Pandas, Seaborn, Matplotlib, statsmodels, scikit-learn_


## Project Pipeline
- Reading and Understanding Data.
- Visualising the Data.
- Data Preparation.
- Model Building.
- Residual Analysis.
- Making predictions using final model.
- Model Evaluation.


## Result
In this notebook I implemented Linear Regression for a machine learning supervised regression task. BoomBikes company can use this model in new market as it possess 82.0% accuracy in predicting the counts of shared bikes.
