# Credit Card Fraud Detection

## Introduction
In this case study, we will conduct exploratory data analysis using Pandas and Seaborn to find driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default. We will also develop a basic understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers.


## Problem Statement
The loan providing companies find it hard to give loans to the people due to their insufficient or non-existent credit history. Because of that, some consumers use it as their advantage by becoming a defaulter.



## Business Objective
This case study aims to identify patterns which indicate if a client has difficulty paying their installments which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. This will ensure that the consumers capable of repaying the loan are not rejected. Identification of such applicants using EDA is the aim of this case study.

Final recommandation of this case study is [here](https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Loan.pptx)
 
 
 
## Project Pipeline
#### The project pipeline can be briefly summarized in the following 9 steps:
 - Data Understanding :
     - Here, you need to load the data and understand the features present in it. 
     - This would help you to choose the features and get insights out of it.
 - Handling missing values :
     - Drop those features whose missing values are so high. Lets say, 50%-55% as per industry standards values.
     - Based on datatype of feature impute them using mean or median, mode. 
 - Check the data-type : 
     - To ensure that data collected in the preferred format.
 - Check for outliers and treat them : 
     - Numerical features are visualized using a boxplot and distribution plot.
     - We handled outlier by capping, removing data. Data removed hasn't affected the analysis.
 - Binning on continous variable : 
     - Binning the data took the analysis a step forward. 
     - Binning features like Age, Credit amount, realtive population brought a useful insights to classify defaulter/fraud.
 - Check for data imbalance : 
    - Visualize the count of defaulter to non-defaulter using Pie-Chart.
    - For every 11 clients, one is a defaulter.
 - Univariate analysis : 
    - The purpose of this analysis is to derive the data, define and summarize it, and analyze the pattern present in it.
 - Bivariate analysis : 
    - Using bivariate analysis helps to know the linear correlation visually, or how well a feature is explained using in addition to other feature.
 - Business Insights :
    - Here we discuss about the important features contributed to classify defaulter from non-defaulter.
    - Statagies for approval of credit card loan to non-defaulter.

#### _Tools: Numpy, Pandas, Seaborn, Matplotlib_


### Defaulter Vs Non-defaulter
<p align="center"><img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/Class%20Imbalance.png' width = 450><p>

- For every `target(target=1)` there at atmost 11 counts of `target(target=0)`.
<details>
  <summary><strong> Click to see some exploratory data analysis </strong></summary>
    
   `Age Vs GoodsPrice`
   <p float="left" align='center'>
  <img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/Age.png' width = 600>
  <img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/goods%20price.png' width = 600>
<p>
   
* Defaulters purchases or loan credited is high in range of 0 to 50,000.   
* we have to note that customer with payment difficulties having in between 31 to 50 years.
   
   
`Income Vs Population`
   <p float="left" align='center'>
  <img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/Income.png' width = 450>
  <img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/Relative Population.png' width = 450>
<p>
   
`Correlation Matrix`

 Defaulter Vs Non-Defaulter
   <p float="left" align='center'>
  <img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/CorrelationMatrix-Defaulter.png' width = 450>
  <img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/CorrelationMatrix-NonDefaulter.png' width = 450>
<p>
   
     
 `Heatmap`
   
Defaulter Vs Non-Defaulter
    <p float="left" align='center'>
  <img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/Heatmap-Defaulter.png' width = 450>
  <img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/Heatmap-NonDefaulter.png' width = 450>
<p>
   
   
`Loan Status`
1. Education
   <p align="center"><img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/Loan%20Status(Education).png' width = 500><p>
   
   - Here we can see that Secondary/ Secondary special is more effective in every case.
   
   
2. Occupation  
   <p align="center"><img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/Loan%20Status(Occupation).png' width = 500><p>
 
   - Here laborers are getting most refused and most approved loans. And aslo Sales staff is also getting the second most refused and approved loans.

3. Income
      <p align="center"><img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/Loan%20Status(Income).png' width = 500><p>
      
      - Here we can see that the working type people are applying more loans as compare to others and also Commercial associates people are taking more loans.
      
   
4. Family Status
  <p align="center"><img src = 'https://github.com/DakshinGowda/DataScience-Projects/blob/main/Credit-Card-Loan/Images/Loan%20Staus(Family%20Status).png' width = 500><p>
   
   - Here we can see that the Married people are applying and taking loans more than the others.
</details>
  



