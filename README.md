## Customer churn prediction

Customer attrition, also known as customer churn, customer turnover, or customer defection, is the loss of clients or customers.

Telephone service companies, Internet service providers, pay TV companies, insurance firms, and alarm monitoring services, often use customer attrition analysis and customer attrition rates as one of their key business metrics because the cost of retaining an existing customer is far less than acquiring a new one. Companies from these sectors often have customer service branches which attempt to win back defecting clients, because recovered long-term customers can be worth much more to a company than newly recruited clients.

Predictive analytics use churn prediction models that predict customer churn by assessing their propensity of risk to churn. Since these models generate a small prioritized list of potential defectors, they are effective at focusing customer retention marketing programs on the subset of the customer base who are most vulnerable to churn.

In this project I aim to perform customer survival analysis and build a model which can predict customer churn. I also aim to build an app which can be used to understand why a specific customer would stop the service and to know his/her expected lifetime value.

## Final App

  ![Screenshot 2023-11-22 162709](https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/57c3a583-02ee-4334-b679-c3d554a4155a)

## Customer survival Analysis

Survival Analysis: Survival analysis is generally defined as a set of methods for analyzing data where the outcome variable is the time until the occurrence of an event of interest. The event can be death, occurrence of a disease, marriage, divorce, etc. The time to event or survival time can be measured in days, weeks, years, etc.

For example, if the event of interest is heart attack, then the survival time can be the time in years until a person develops a heart attack.

Objective: The objective of this analysis is to utilize non-parametric and semi-parametric methods of survival analysis to answer the following questions.

- How the likelihood of the customer churn changes over time?

- How we can model the relationship between customer churn, time, and other customer characteristics?

- What are the significant factors that drive customer churn?

- What is the survival and Hazard curve of a specific customer?

- What is the expected lifetime value of a customer?
  
Kaplan-Meier Survival Curve:

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/03f9b673-b52b-46d3-bb95-391e277759d8" width="400" height="300">
</p>

From above graph, we can say that

- AS expected, for telcom, churn is relatively low. The company was able to retain more than 60% of its customers even after 72 months.

- There is a constant decrease in survival probability probability between 3-60 months.

- After 60 months or 5 years, survival probability decreases with a higher rate.
  
**Log-Rank Test:** 

Log-rank test is carried out to analyze churning probabilities group wise and to find if there is statistical significance between groups. The plots show survival curve group wise.

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/1498fd0b-716f-4670-b738-ebef8049d511" width="400" height="300">
</p>

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/1f9ca7a7-99f5-4156-8f31-2d52e203f6b8" width="250" height="200"/> 
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/49da2cd0-98d2-45d3-bc43-1068396346d8" width="250" height="200"/>
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/43ad1415-b53c-4ef1-a3a8-9250f1bef01d" width="250" height="200"/> 
</p>

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/5bc081d9-8c39-426b-a576-38d8a3345e23" width="250" height="200"/> 
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/1bcd866f-4e68-4aab-afc3-a7ac249de088" width="250" height="200"/>
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/1965a084-8733-4bc6-906f-0ef4ceedd7b7" width="250" height="200"/> 
</p>

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/831d98c0-25ec-4df5-b2c6-bfe06b74ee5f" width="250" height="200"/> 
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/0fbf8084-35ff-4e87-a62b-c499b836101d" width="250" height="200"/> 
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/45113e4d-6c8c-4679-a60a-adc93965077a" width="250" height="200"/> 
</p>

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/52f2eb12-771f-4ffe-85e9-84a22bfe1c26" width="250" height="200"/> 
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/705a9b0e-4fc5-4707-ac4d-ca47de2a211c" width="250" height="200"/>
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/a009b5a1-ef80-45f4-90d7-aa8041cc4687" width="250" height="200"/> 
</p>

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/3a6b0385-48ff-47fb-bdab-188d044b0909" width="250" height="200"/>
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/fe4f35e1-c527-4929-85aa-daee8c5e7acb" width="250" height="200"/> 
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/ee3336de-33bf-47bd-9a21-f25d7c5f1d73" width="250" height="200"/>
</p>


From above graphs we can conclude following:

- Customer's Gender and the phone service type are not indictive features and their p value of log rank test is above threshold value 0.05.
- If customer is young and has a family, he or she is less likely to churn. The reason might be the busy life, more money or another factors.
- If customer is not enrolled in services like online backup, online security, device protection, tech support, streaming Tv and streaming movies even though having active internet service, the survival probability is less.
- The company should traget customers who opt for internet service as their survival probability constantly descreases. Also, Fiber Optilc type of Internet Service is costly and fast compared to DSL and this might be the reason of higher customer churning.
- More offers should be given to customers who opt for month-to-month contract and company should target customers to subscribe for long-term service.
- If customer's paying method is automatic, he or she is less likely to churn. The reason is in the case of electronic check and mailed check, a customer has to make an effort to pay and it takes time.

**Survival Regression:**

I use cox-proportional hazard model to perform survival regression analysis on customer data. This model is used to relate several risk factors or exposures simultaneously to survival time. In a Cox proportional hazards regression model, the measure of effect is the hazard rate, which is the risk or probability of suffering the event of interest given that the participant has survived up to a specific time. The model fits the data well and the coefficients are shown below.

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/e554d265-d2a3-4d76-b7b9-35e2eb35c249" width="750" height="500"/>
</p

Using this model we can calculate the survival curve and hazard curve of any customer as shown below. These plots are useful to know the remaining life of a customer.

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/4a1b1321-a81f-4004-bc89-9a28d075772c" width="400" height="300"/>
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/edbd5cba-6e3b-4d7a-99c1-b362549338cf" width="400" height="300"/>
</p>

**Customer Lifetime Value:**

To calculate customer lifetime value, I would multiply the Monthly charges the customer is paying to Telcom and the expected life time of the customer.

I utilize the survival function of a customer to calculate its expected life time. I would like to be little bit conservative and consider the customer is churned when the survival probability of him is 10%.

## Customer Churn prediction

I aim to implement a machine learning model to accurately predict if the customer will churn or not.

### Analysis

**Churn and Tenure Relationship:**

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/6b8bea04-a7d5-4bbd-9e95-2c2eb4659c85" width="600" height="300"/>
</p>

- As we can see the higher the tenure, the lesser the churn rate. This tells us that the customer becomes loyal with the tenure.

<br />

**Tenure Distrbution by Various Services:**

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/11d5e504-e000-4a4e-9818-f14017d8267f" width="340" height="250"/>
</p>

- When the customers are new they do not opt for various services and their churning rate is very high. This can be seen in above plot for Streaming Movies and this holds true for all various services.

<br />

**Internet Service By Contract Type:**

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/ad42d0ad-df8d-4628-a8fe-ca6232285939" width="360" height="250"/>
</p>

- Many of the people of who opt for month-to-month Contract choose Fiber optic as Internet service and this is the reason for higher churn rate for fiber optic Internet service type.

<br />

**Payment method By Contract Type:**

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/69327bb0-2ea4-44aa-ad98-f55a315e50cf" width="500" height="250"/>
</p>

- People having month-to-month contract prefer paying by Electronic Check mostly or mailed check. The reason might be short subscription cancellation process compared to automatic payment.

<br />

**Monthly Charges:**

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/eaba54de-be3c-4ca1-ba05-da243f9e7107" width="300" height="220"/>
</p>

- As we can see the customers paying high monthly fees churn more.

<br />

### Modelling

For the modelling, I will use tress based Ensemble method as we do not have linearity in this classification problem. Also, we have a class imbalance of 1:3 and to combat it I will assign class weightage of 1:3 which means false negatives are 3 times costlier than false positives. I built a model on 80% of data and validated model on remaining 20% of data keeping in mind that I do not have data leakage. The random forest model has many hyperparameters and I tuned them using Grid Search Cross Validation while making sure that I do not overfit.

The final model resulted in 0.62 F1 score and 0.85 ROC-AUC. The resulting plots can be seen below.

<p align="center">
<img src="https://github.com/Pramit2021/Customer_churn_prediction/assets/93142399/96e6082a-6f0d-4c05-af32-a1ef1c152065" width="600" height="500"/>
</p>

From the feature importance plot, we can see which features govern the customer churn.

## Flask app

I saved the final tuned Random Forest model and deployed it using Flask web app. Flask is a micro web framework written in Python.  It is designed to make getting started quick and easy, with the ability to scale up to complex applications. I saved the shap value explainer tuned using random forest model to show shap plots in app. I have also utilized the cox-proportional hazard model to show survival curve and hazard curve, and to calculate expected customer lifetime value. 

The final app shows churning probability, gauge chart of how severe a customer is and shap values based on customer's data. The final app layout can be seen above.  


## Created by

- Pramit Ray
- Vaibhav Malhotra
