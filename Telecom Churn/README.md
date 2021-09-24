# Telecom Churn

## Business Problem Overview
In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. 
In this highly competitive market, the telecommunications costs 5-10 times more to acquire a new customer than to retain an existing one, 
customer retention has now become even more important than customer acquisition. 

**_For many incumbent operators, retaining high profitable customers is the number one business goal_**.

To reduce customer churn, telecom companies need to predict which customers are at high risk of churn. In this project, you will analyse customer-level data of a 
leading telecom firm, build predictive models to identify customers at high risk of churn and identify the main indicators of churn.

## Understanding and Defining Churn
There are two main models of payment in the telecom industry - postpaid (customers pay a monthly/annual bill after using the services) and 
prepaid (customers pay/recharge with a certain amount in advance and then use the services). 
In the postpaid model, when customers want to switch to another operator, they usually inform the existing operator to terminate the services, and you directly know that this is an instance of churn. 
However, in the prepaid model, customers who want to switch to another network can simply stop using the services without any notice, and it is hard to know whether someone has actually churned or is simply not using the services temporarily (e.g. someone may be on a trip abroad for a month or two and then intend to resume using the services again). Thus, churn prediction is usually more critical (and non-trivial) for prepaid customers, and the term ‘churn’ should be defined carefully. Also, prepaid is the most common model in India and southeast Asia, while postpaid is more common in Europe in North America. 
This project is based on the Indian and Southeast Asian market.

## High-value Churn
In the Indian and the southeast Asian market, approximately 80% of revenue comes from the top 20% customers (called high-value customers).
Thus, if we can reduce churn of the high-value customers, we will be able to reduce significant revenue leakage.

In this project, we will define high-value customers based on a certain metric (mentioned later below) and predict churn only on high-value customers.


## Understanding Customer Behaviour During Churn
Customers usually do not decide to switch to another competitor instantly, but rather over a period of time (this is especially applicable to high-value customers). 
In churn prediction, we assume that there are three phases of customer lifecycle :

- The ‘good’ phase: In this phase, the customer is happy with the service and behaves as usual.
- The ‘action’ phase: The customer experience starts to sore in this phase, for e.g. he/she gets a compelling offer from a competitor, faces unjust charges, becomes unhappy with service quality etc. In this phase, the customer usually shows different behaviour than the ‘good’ months. Also, it is crucial to identify high-churn-risk customers in this phase, since some corrective actions can be taken at this point (such as matching the competitor’s offer/improving the service quality etc.)
- The ‘churn’ phase: In this phase, the customer is said to have churned. We define churn based on this phase. Also, it is important to note that at the time of prediction (i.e. the action months), this data is not available to us for prediction. Thus, after tagging churn as 1/0 based on this phase, we discard all data corresponding to this phase.

In this case, since we are working over a four-month window, the first two months are the ‘good’ phase, the third month is the ‘action’ phase, while the fourth month is the ‘churn’ phase.

_Tools: Numpy, Pandas, Seaborn, Matplotlib, scikit-learn, scipy_


## Steps for Model Building
- Data Cleaning
  - Handling missing data.
  - Analyse the hidden pattern behind the recharge amount and its corresponding date.
  - Remove unwanted columns based on unique counts present in tbe features.

- High-value customers.
 
- Data Pre-processing
  - Derive churn feature(Target feature) : Churn feature is derived using Total calls and Net data consumption in month of September.
  - Multicolllinearity : Drop highly correlated features by choosing cut-off pearson correlation coefficient as 0.8 .

- Data Visualization 
  - Univariate Analysis : The purpose of this analysis is to derive the data, define and summarize it, and analyze the pattern present in it.
  - Bivariate Analysis : Using bivariate analysis helps to know the how well a feature is explained using in combination with other feature.

- Class Imbalance 
  - Handling class imbalance using SMOTE Technique.

- Outlier Treatment
  - Plot distribution of the numerical features examine the skewness.
  - Reduced skewness using Winsorization Transformation technique.

- Model Building
  - Feature Scaling : Numerical features are scaled using Standardization technique.
  - Dimensiona Reduction : Reduce the number of variables using PCA.
  - Hyper-Parameter tuning : Tuning hyper-paramters on Logistic Regression, Random Forest classifier and XGBoost classifier models using Kfold cross-validation until you get the desired level of performance on the given dataset.
  - Feature Importance : Plot top 30 features that are useful in predicting  customer churn.

- Evaluation Metrics
  - Evaluate the models using appropriate evaluation metrics. 
  
**Note that it is more important to identify churners than the non-churners accurately - choose an appropriate evaluation metric which reflects this business goal**.
 
Finally, a Random Forest Classifier model is choosed based on Sensitivity and Specificiy as an evaluation metric.

### Scores

Best single models:

| Model                  | Sensitivity | Specificity |  AUC | 
| :--------------------: | :----------:| :----------:| :---:|
| RandomForestClassifier |     0.90	   |     0.91    | 0.91 |
| XGB Classifer          |     0.89    |     0.87    | 0.88 | 
| Logistic Regression	   |     0.85    |    0.85     | 0.85 |


## Document
The dataset can be downloaded from [here](https://drive.google.com/file/d/1SWnADIda31mVFevFcfkGtcgBHTKKI94J/view)

Telecom churn.ipynb [link](https://github.com/DakshinGowda/DataScience-Projects/blob/main/Telecom%20Churn/Telecom%20churn.ipynb) : The python file.

Data+Dictionary-+Telecom+Churn+Case+Study.xlsx [link](https://github.com/DakshinGowda/DataScience-Projects/blob/main/Telecom%20Churn/Data%2BDictionary-%2BTelecom%2BChurn%2BCase%2BStudy.xlsx) : Data Dictionary.

## Team
- [Dakshin](https://github.com/DakshinGowda)
- [Siddhant Singh](https://github.com/siddhant-official)

