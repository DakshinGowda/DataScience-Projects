# Credit Card Fraud Detection
## Problem Statement
This case study aims to identify patterns which indicate if a client has difficulty paying their instalments which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. This will ensure that the consumers capable of repaying the loan are not rejected. Identification of such applicants using EDA is the aim of this case study.

## Understanding and Defining Fraud
   #### Credit card fraud is any dishonest act and behaviour to obtain information without the proper authorization from the account holder for financial gain. Among different ways of frauds, Skimming is the most common one, which is the way of duplicating of information located on the magnetic strip of the card. Apart from this, the other ways are:
   - Manipulation/alteration of genuine cards
   - Creation of counterfeit cards
   - Stolen/lost credit cards
   - Fraudulent telemarketing
 
 #### _Tools: Numpy, Pandas, Seaborn, Matplotlib_
 
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
    - For every 1 in 11 client is a non-defaulter.
 - Univariate analysis : 
    - The purpose of this analysis is to derive the data, define and summarize it, and analyze the pattern present in it.
 - Bivariate analysis : 
    - Using bivariate analysis helps to know the linear correlation visually, or how well a feature is explained using in addition to other feature.
 - Business Insights :
    - Here we discuss about the important features contributed to classify defaulter from non-defaulter.
    - Statagies for approval of credit card loan to non-defaulter.

