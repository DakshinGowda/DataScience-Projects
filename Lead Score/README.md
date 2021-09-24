# Lead Scoring

## Problem Statement
#### An education company named X Education sells online courses to industry professionals. On any given day, many professionals who are interested in the courses land on their website and browse for courses.

The company markets its courses on several websites and search engines like Google. Once these people land on the website, they might browse the courses or fill up a form for the course or watch some videos. When these people fill up a form providing their email address or phone number, they are classified to be a lead. Moreover, the company also gets leads through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc. Through this process, some of the leads get converted while most do not. The typical lead conversion rate at X education is around 30%.

Now, although X Education gets a lot of leads, its lead conversion rate is very poor. For example, if, say, they acquire 100 leads in a day, only about 30 of them are converted. To make this process more efficient, the company wishes to identify the most potential leads, also known as ‘Hot Leads’. If they successfully identify this set of leads, the lead conversion rate should go up as the sales team will now be focusing more on communicating with the potential leads rather than making calls to everyone.

<p align="center">
  <img src='https://user-images.githubusercontent.com/68459881/134554756-23147780-86b0-4442-8885-d4e0f14ff35c.jpg'>
</p>

## Lead Conversion Process 
Demonstrated as a funnel As you can see, there are a lot of leads generated in the initial stage (top) but only a few of them come out as paying customers from the bottom. In the middle stage, you need to nurture the potential leads well (i.e. educating the leads about the product, constantly communicating etc. ) in order to get a higher lead conversion.

#### X Education has appointed you to help them select the most promising leads, i.e. the leads that are most likely to convert into paying customers. The company requires you to build a model wherein you need to assign a lead score to each of the leads such that the customers with higher lead score have a higher conversion chance and the customers with lower lead score have a lower conversion chance. The CEO, in particular, has given a ballpark of the target lead conversion rate to be around 80%.



## Goals of the Case Study
  - #### Build a logistic regression model to assign a lead score between 0 and 100 to each of the leads which can be used by the company to target potential leads. A higher score would mean that the lead is hot, i.e. is most likely to convert whereas a lower score would mean that the lead is cold and will mostly not get converted.
  - #### The model is interpretable to adjust to if the company's requirement changes in the future.
  - #### Final recommandation is included in [leadscore ppt](https://github.com/DakshinGowda/DataScience-Projects/blob/main/Lead%20Score/LeadScore(PPT).pdf)

## Project Pipeline
The project pipeline can be briefly summarized in the following steps:
#### • Data Understanding
   Here, you need to load the data and understand the features present in it. This would help you choose the features that you will need for your final model.
#### • Exploratory data analytics (EDA)
   Normally, in this step, you need to perform univariate and bivariate analyses of the data, followed by feature transformations, if necessary. For the current data set need to perform Z-scaling.
#### • Model-Building
   This is the final step at which we train 9000 rows and left out with 15 features to train using logistic regression algorithm.
#### • Model Evaluation
   Evaluate the models using appropriate evaluation metrics. Choose an appropriate evaluation metric which reflects this business goal.
