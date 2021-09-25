# House Prices prediction using Advanced Regression Techniques

## Introduction
There are several factors that influence the price a buyer is willing to pay for a house. Some are apparent and obvious and some are not. Nevertheless, a rational approach facilitated by machine learning can be very useful in predicting the house price. A large data set with 81 different features (like lot area,  overall condition, garage area etc) along with their prices are provided for residential homes in Australia. The challenge is to learn a relationship between the important features and the price and use it to predict the prices of a new set of houses.

## Problem Statement
A US-based housing company named Surprise Housing data analytics to purchase houses at a price below their actual values and flip them on at a higher price. 
The company is looking at prospective properties to buy to enter the market. 
The company wants to know the following things about the prospective properties:
  - Which variables are significant in predicting the price of a house, and
  - How well those variables describe the price of a house.

## Business Goal 
You are required to model the price of houses with the available independent variables. 
This model will then be used by the management to understand how exactly the prices vary with the variables. 
They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. 
Further, the model will be a good way for management to understand the pricing dynamics of a new market.

_Tools: Numpy, Pandas, Seaborn, Matplotlib, scikit-learn_


## Project Pipeline

- Exploratory data analysis
  - Plot distribution of the numerical features examine the skewness and plot correlation matrix between the features.
  - Plot distribution of categorical features to examine the imbalance in feature.
  - <details>
    <summary><strong> Click to Visualize the conditon of the building over a period of years. </strong></summary>
    <p align="center"><img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/House%20Price%20Prediction/Images/Age%20Built.png' width = 700><p>
    </details>

- Preprocessing of data
  - <details>
    <summary><strong> Filling missing Data. </strong></summary>
    <p float="left" align='center'>
      <img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/House%20Price%20Prediction/Images/Missing%20data%20(Graph).png' width = 800>
      <img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/House%20Price%20Prediction/Images/Missing%20data%20(df).png' width = 400>
    <p>
    </details>
  
  - <details>
    <summary><strong> Remove skewenes of Target feature using log Transformation. </strong></summary>
    <p float="left" align='center'>
      <img title='before' src='https://github.com/DakshinGowda/DataScience-Projects/blob/main/House%20Price%20Prediction/Images/SkewTarget%20(Before).png' alt="Girl in a jacket" width = 400>
      <img src='https://github.com/DakshinGowda/DataScience-Projects/blob/main/House%20Price%20Prediction/Images/SkewTarget%20(After).png' width = 400>
    <p>
    </details>

  
  - Handle imbalanced categorical features.
  - Feature selection.

- Feature Engineering
  - Engineering new features by analysing the hidden paterns within them.
  - Multicollinearity check among the independent variables. Drop highly correlated features by choosing cut-off pearson correlation coefficient as 0.8 .
  - Create Indicator variable.
  - Label Encoding features related to Quality and Condtion.
  - Scaling features using Robust Scaler.

- Modelling
  - Feature Extraction using Recursive Feature Elimination(RFE) to obtain top 50 features.
  - Fitting different models - Linear Regression, Ridge & Lasso regualization techniques on the cleaned data.
  - Hyperparameter tuning on Ridge and Lasso models using Kfold cross-validation until you get the desired level of performance on the given dataset.
  - Optimal value of alpha for Ridge and Lasso models.
  - Best model is choosed among 2 models built by predicting the house price on test set.

### Scores

Best single models:

| Model    | Train    | Test  	 | 
| :-------:| :-------:| :-------:|
| Lasso    | 0.845300 | 0.842063 |
| Ridge    | 0.844266 | 0.838802 |

