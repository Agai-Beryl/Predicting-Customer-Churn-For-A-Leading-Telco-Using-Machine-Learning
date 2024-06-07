## PREDICTING CUSTOMER CHURN RATE FOR SYRIATEL TELCO:A MACHINE LEARNING APPROACH
### BUSINESS UNDERSTANDING
#### Overview
SyriaTel is the leading communications company in the region and most customers are happy with its services.
However,recently,they have been facing a spike in customer churn.
As the lead data scientist tasked to analyze this trend and predict the churn rate,I understand that this task is crucial in helping Syriatel enhance customer retention,establish market dominance,foster customer obsession and improve their revenue.

#### Stakeholders
The possible stakeholders in this project are:

- SyriaTel Executive Leadership: Interested in how they can use these insights to ensure customer obession and revenue increase.

- Customer Retention Team: These insights help them notice the customers who are likely to churn and sway them into staying.

- Customer Sales & Marketing Department: The insights from churn prediction helps them personalize products and services to customers.

- #### Problem Statement

- At SyriaTel,the issue of customer churn has been an urgent matter that needs immediate intervention.We will perform Root Cause Analysis by using data driven approach and machine learning.Some of the potential challenges causing the massive spike in churn may be related to pricing,cutomer service experience,product quality among others.We will get to the bottomof it and provide insights that enable our client to maintain market dominance,foster customer obsession,enhance customer retention and improve their revenue.


- #### Objectives
- Our main objective is to identify the factors driving customer churn at SyriaTel and build a predictive model with atleast 80% precision to enable the implementation of targeted strategies for retention and improved business outcomes.
- Build a robust prediction model with a precision rate of 0.8 and above.

- Identify key factors that leads to customer churn.

- Provide reliable insights to our client to enable them mitigate the issue of churn.

- Demonstrate the value of the prediction model and how much it will help our client meet their business needs.

- ### DATA UNDERSTANDING
- Our dataset which is bigml_59c28831336c6604c800002a.csv is sourced from Kaggle

It has 3333 labels and 21 features.

It does not have any missing values at first glance.

The datatypes are mainly float (8 features),interger(8 features),object (4 features) and boolean (1 feature),in that descending order.

There are 17 continuos features and 4 categorical features

The target variable is Churn andthe rest are predictor variables.

### DATA PREPARATION
We dropped the phone number feature due to ethical reasons.

One hot encoded the categorical variables.

Removed outliers.

Dropped highly correlated variables

### EXPLORATORY DATA ANALYSIS (EDA)

Most churners are from area code 1&2
Customers that make more customer service calls are the highest churners.
Customers with an international plan churn more than those without.
Churners have higher day-time usage and charges.
Churn customers mostly have zero voice mail messages, while their counter parts have more.
![image](https://github.com/Agai-Beryl/Predicting-Customer-Churn-For-A-Leading-Telco-Using-Machine-Learning/assets/162470891/0fda34a4-5ea5-4afd-9345-303c38735878)

- 

