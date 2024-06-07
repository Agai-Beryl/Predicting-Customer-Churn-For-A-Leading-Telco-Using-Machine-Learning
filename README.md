## PREDICTING CUSTOMER CHURN RATE FOR SYRIATEL TELCO:A MACHINE LEARNING APPROACH

![Churn](https://github.com/Agai-Beryl/Predicting-Customer-Churn-For-A-Leading-Telco-Using-Machine-Learning/assets/162470891/dae77bfa-e17c-4c77-aba8-f11ca42e7915)

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

 #### Problem Statement

- At SyriaTel,the issue of customer churn has been an urgent matter that needs immediate intervention.We will perform Root Cause Analysis by using data driven approach and machine learning.Some of the potential challenges causing the massive spike in churn may be related to pricing,cutomer service experience,product quality among others.We will get to the bottomof it and provide insights that enable our client to maintain market dominance,foster customer obsession,enhance customer retention and improve their revenue.


 #### Objectives
- Our main objective is to identify the factors driving customer churn at SyriaTel and build a predictive model with atleast 80% precision to enable the implementation of targeted strategies for retention and improved business outcomes.
- Build a robust prediction model with a precision rate of 0.8 and above.

- Identify key factors that leads to customer churn.

- Provide reliable insights to our client to enable them mitigate the issue of churn.

- Demonstrate the value of the prediction model and how much it will help our client meet their business needs.

 ### DATA UNDERSTANDING
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

![Churn vs area](https://github.com/Agai-Beryl/Predicting-Customer-Churn-For-A-Leading-Telco-Using-Machine-Learning/assets/162470891/f3015517-6d99-43bb-911e-b27f67080988)
![Churn vs customer service calls](https://github.com/Agai-Beryl/Predicting-Customer-Churn-For-A-Leading-Telco-Using-Machine-Learning/assets/162470891/b2435bc1-081f-4969-a0a1-cc07cd41287b)


### MODELING

We scaled  the data,split it into 80-20 train test split and fixed class imbalance using SMOTE.

We built 5 models and tuned their hyperparameters using GridSearchCV and cross validation.

The perfomance metrics evaluated were:

 - Accuracy

 - Precision

 - Recall

 - F1

 - ROC

 - AUC

The models  performed well  in this descending  order(from best to least performer):

 - XGBoost

 - Random Tree Clasifier

 - Decision Tree Classifier

 - KNN Classifier

 - Logistic Regression Classifier

   ![XGBoost](https://github.com/Agai-Beryl/Predicting-Customer-Churn-For-A-Leading-Telco-Using-Machine-Learning/assets/162470891/47dae8ea-93fa-40e3-a069-ce4ed1ad3e3d)

### OBSERVATIONS

The top features impacting churn are :

- Customer service calls: The number of customer service calls made by customers has the highest importance as an indicator of potential churn.

- Total day minutes: This feature indicates that the daytime minutes offered plays a crucial role in determining customer churn.

- Number vmail messages : This feature contributes notably to the model’s predictions and likely represents an important factor, albeit secondary to the top two, in understanding customer churn.

- Total eve minutes: While less influential than the top three features, it still holds considerable importance and may represent additional customer attributes or behaviors affecting churn.

- Total night minutes: This feature has a moderate impact, indicating it likely captures some relevant but not dominant factors related to churn.

- Total eve calls: Its contribution is less pronounced, suggesting it may represent more specific or less frequent factors influencing churn.

- State: Its relatively lower importance suggests it might be capturing ancillary factors or interactions that influence churn.

- The other features like total day calls,total international calls,account length,total night calls and total international minutes have minimum impact on churn,meaning they are non dominant factors.

- From that point,its interesting to note that area code , lack of an international plan and the other remaining features were not considered as factors impacting churn rate by the XGBoost model

  ### RECOMMENDATIONS

  Based on the findings, SyriaTel can take the following actions to reduce customer churn and minimize revenue loss:

- Customer Service Calls:
Enhance customer service training for the representatives.

Reduce response times.

Implement proactive customer satisfaction surveys and follow-up calls to address potential issues before they lead to churn.

- Total Day Minutes:
Introduce flexible and affordable day minute plans to cater to heavy daytime users.

Offer incentives or discounts for plans with higher daytime minutes to retain customers.

- Number of Voicemail Messages:
Promote the use of voicemail services by highlighting their benefits.

Offer bundled packages with enhanced voicemail features to add value to customer subscriptions.

-Total Evening Minutes:
Develop evening-specific plans or promotions to attract customers who use services predominantly during these hours.

Monitor evening usage patterns to tailor future offerings better.

- Total Night Minutes:
Introduce plans that offer competitive rates for night usage.

Engage night-time users through targeted marketing campaigns and personalized offers.

- Total Evening Calls:
Investigate customer segments that frequently make evening calls and create tailored engagement strategies for them.

Offer loyalty rewards for consistent usage.

- State:
Conduct regional analyses to identify any state-specific issues or preferences.

Customize marketing and service offerings based on regional characteristics.

- Total Day Calls, Total International Calls, Account Length, Total Night Calls, Total International Minutes:
Ensure these features are optimized for efficiency and customer satisfaction. Periodically review these features to ensure they meet customer needs without significantly impacting operational costs.

- Area Code and Lack of an International Plan:
Focus less on these variables for churn prevention strategies because they dont directly predict the churn. However, continue monitoring them for any emerging patterns and ensure comprehensive service coverage and international plan options are available.

### CONCLUSION

We have successfully identified key factors influencing customer churn using our best performing model; the XGBoost model. Features such as customer service calls and total day minutes emerged as the most significant predictors of churn. Based on these insights, targeted recommendations were provided to improve customer retention. Implementing these strategies can help reduce churn rates, enhance customer satisfaction, and ultimately drive business growth. Continuous monitoring and adjustment of these strategies will ensure sustained effectiveness and adaptability to evolving customer needs.



