# Bank Customer Churn Prediction

## Project Overview

Customer churn represents a major challenge for financial institutions. When customers decide to leave a bank, the institution loses not only immediate revenue but also long-term customer value. Retaining existing customers is significantly more cost-effective than acquiring new ones, making churn prediction a critical component of customer relationship management.

This project aims to develop a machine learning system capable of identifying customers who are at risk of leaving the bank. By analyzing behavioral, demographic, and transactional data, the model can help financial institutions anticipate churn and implement targeted retention strategies.

The final objective is to transform raw customer data into actionable insights that support proactive decision-making and improve customer retention.

---

# Business Problem

Customer attrition directly impacts the profitability of financial institutions. When a customer leaves a bank, the organization loses future revenue streams, potential cross-selling opportunities, and customer lifetime value.

However, customer churn rarely occurs randomly. It is often preceded by behavioral signals such as decreased engagement, reduced transaction activity, or increasing account inactivity.

Being able to detect these patterns early allows banks to intervene with personalized retention strategies such as:

- loyalty programs
- targeted promotions
- proactive customer support
- financial incentives

Therefore, predicting customer churn is a powerful tool for improving customer retention and maintaining long-term profitability.

---

# Project Objective

The objective of this project is to build a predictive machine learning model that can accurately determine whether a customer is likely to churn.

The system uses historical customer data to identify patterns associated with customer attrition. By leveraging these patterns, the model can estimate the probability that a given customer will leave the bank.

The final model can support decision-making processes by enabling banks to prioritize retention efforts toward customers who are most at risk.

---

# Dataset Description

The dataset contains detailed information about bank customers, including demographic attributes, account information, and transaction behavior.

These features allow the model to capture different dimensions of customer behavior and engagement.

### Key Variables

The dataset includes several categories of variables:

### Customer Demographics

- Customer_Age
- Gender
- Marital_Status
- Income_Category
- Education_Level
- Dependent_count

These variables describe the personal and socioeconomic characteristics of customers.

### Account Information

- Months_on_book
- Credit_Limit
- Total_Relationship_Count
- Card_Category

These variables describe the customer's relationship with the bank and the type of financial products they hold.

### Customer Behavior

- Months_Inactive_12_mon
- Contacts_Count_12_mon
- Avg_Utilization_Ratio

These features provide insights into customer engagement and account activity.

### Transaction Activity

- Total_Trans_Ct
- Total_Trans_Amt
- Total_Amt_Chng_Q4_Q1
- Total_Ct_Chng_Q4_Q1
- Total_Revolving_Bal

Transaction-related variables are particularly important because they capture the customer's level of financial activity and engagement with the bank.

### Target Variable

The target variable is:

**Attrition_Flag**

This variable indicates whether the customer has churned or remains an active client of the bank.

For modeling purposes, the target variable was transformed into a binary numerical format:

- 1 → customer churned
- 0 → customer retained

---

# Data Exploration and Insights

An exploratory data analysis (EDA) was conducted to better understand the dataset and identify potential patterns related to customer churn.

The analysis revealed that customer behavior plays a critical role in predicting attrition.

Several important patterns emerged:

- Customers with lower transaction counts tend to churn more frequently.
- Higher inactivity periods are strongly associated with customer attrition.
- Customers with fewer relationships with the bank are more likely to leave.
- Lower engagement with credit card usage can indicate churn risk.

These insights highlight the importance of behavioral indicators in understanding customer retention.

---

# Feature Engineering

Before training the machine learning models, several preprocessing and feature engineering steps were performed.

Categorical variables such as gender, marital status, education level, and card category were converted into numerical representations using encoding techniques. This transformation allows machine learning algorithms to process categorical information effectively.

The target variable **Attrition_Flag** was converted into a binary numerical variable to represent customer churn.

Feature engineering plays a crucial role in improving model performance because it ensures that the dataset contains meaningful representations of customer behavior.

---

# Machine Learning Models

To build a robust predictive system, three different machine learning algorithms were implemented and compared.

Each model represents a different level of complexity and predictive capability.

### Logistic Regression

Logistic Regression was used as the baseline model for this project. It is a widely used statistical method for binary classification problems and offers strong interpretability.

One of the key advantages of logistic regression is that it allows us to analyze the influence of individual variables on the probability of churn through model coefficients.

However, logistic regression assumes a linear relationship between the features and the target variable, which may limit its ability to capture complex patterns in the data.

---

### Random Forest

Random Forest is an ensemble learning method that combines multiple decision trees to improve predictive performance.

By aggregating the predictions of many trees, Random Forest reduces overfitting and captures nonlinear relationships between variables.

In this project, Random Forest significantly improved prediction performance compared to logistic regression and provided useful insights through feature importance analysis.

---

### XGBoost

XGBoost (Extreme Gradient Boosting) is an advanced ensemble learning algorithm based on gradient boosting techniques.

The algorithm builds trees sequentially, where each new tree focuses on correcting the errors made by the previous ones.

This iterative learning process allows XGBoost to capture subtle patterns and interactions between variables, making it one of the most powerful algorithms for structured datasets.

Among the models tested in this project, XGBoost achieved the best predictive performance.

---

# Model Evaluation

Several evaluation metrics were used to assess the performance of the models, including:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

In the context of churn prediction, **recall for the churn class is particularly important**, because failing to detect customers who are about to leave can lead to significant revenue loss.

The comparison of model performance showed that XGBoost achieved the highest predictive accuracy and the strongest ability to correctly identify customers at risk of churn.

---

# Key Drivers of Customer Churn

The analysis revealed that customer behavior variables are the most influential predictors of churn.

The most important factors include:

- Total transaction count
- Transaction amount
- Account inactivity
- Customer-bank interaction frequency
- Total relationship count

These variables reflect customer engagement with the bank's services. Lower engagement typically signals a higher probability of customer attrition.

---

# Business Impact

A reliable churn prediction system can provide significant value to financial institutions.

By identifying high-risk customers early, banks can implement targeted retention strategies such as:

- personalized offers
- loyalty programs
- proactive customer support
- financial incentives

This proactive approach helps reduce customer attrition and increases long-term profitability.

---

# Conclusion

This project demonstrates how machine learning techniques can be used to transform customer data into actionable insights for financial institutions.

By combining exploratory data analysis, feature engineering, and advanced machine learning models, it is possible to build a predictive system capable of identifying customers at risk of churn.

Among the models tested, **XGBoost delivered the best overall performance** and was selected as the final model for customer churn prediction.

The model provides strong predictive capabilities and can support banks in implementing proactive retention strategies.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

---

# Author

Powered by **Zougagh Ayoub**