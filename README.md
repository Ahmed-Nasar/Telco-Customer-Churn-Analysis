# Telco Customer Churn Analysis

**Dashboard ->** [here](https://app.powerbi.com/view?r=eyJrIjoiYzllYTllNWEtZDc4Ny00OTc3LTg3ODAtZjFhZjMxZDlkOTliIiwidCI6IjI1Y2UwMjYxLWJiZDYtNDljZC1hMWUyLTU0MjYwODg2ZDE1OSJ9)

This project provides an in-depth analysis of customer churn in the telecommunications industry. The analysis, conducted using Power BI, focuses on understanding the demographics and account information of high-risk customers to identify factors contributing to churn. This project is intended to help businesses make data-driven decisions to improve customer retention.

| Contents 											 	   	|
| -------- 											 	   	|
| [Project Overview](#Project-Overview)			   	|
| [Dataset Description](#Dataset-Description) 		   		|
| [Columns Description](#Columns-Description)							|
| [EDA Questions](#EDA-Questions)					   		|
| [Data Cleaning](#Data-Cleaning)						   	|
| [KPI Dashboard](#KPI-Dashboard)					|
| [Conclusion](#Conclusion)									|
| [Recommendations](#Recommendations)							   		|

## Project Overview:

The goal of this analysis is to:
- Analyze customer churn data to understand key factors associated with churn.
- Visualize churn rates by demographic and account features.
- Provide insights and recommendations to reduce churn.

## Dataset Description:

The dataset used for this project is publicly available in [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) and contains information on customers, including:
-	**Demographics**: Gender, senior citizen status, partner status, and dependents.
-	**Account Information**: Contract type, payment method, and monthly charges.
-	**Services**: Internet service, online security, device protection, and more.

## Columns Description:

1. `customerID`: A unique identifier for each customer.
2. `gender`: The gender of the customer (Male or Female).
3. `SeniorCitizen`: Indicates whether the customer is a senior citizen (1 = Yes, 0 = No).
4. `Partner`: Indicates whether the customer has a partner (Yes or No).
5. `Dependents`: Indicates whether the customer has dependents (Yes or No).
6. `tenure`: The number of months the customer has stayed with the company.
7. `PhoneService`: Indicates whether the customer has a phone service (Yes or No).
8. `MultipleLines`: Indicates whether the customer has multiple phone lines (Yes, No, or No phone service).
9. `InternetService`: The type of internet service the customer has (DSL, Fiber optic, or No internet service).
10. `OnlineSecurity`: Indicates whether the customer has online security service (Yes, No, or No internet service).
11. `OnlineBackup`: Indicates whether the customer has an online backup service (Yes, No, or No internet service).
12. `DeviceProtection`: Indicates whether the customer has a device protection service (Yes, No, or No internet service).
13. `TechSupport`: Indicates whether the customer has tech support service (Yes, No, or No internet service).
14. `StreamingTV`: Indicates whether the customer has a streaming TV service (Yes, No, or No internet service).
15. `StreamingMovies`: Indicates whether the customer has streaming movies service (Yes, No, or No internet service).
16. `Contract`: The type of contract the customer has (Month-to-month, One year, Two years).
17. `PaperlessBilling`: Indicates whether the customer uses paperless billing (Yes or No).
18. `PaymentMethod`: The payment method used by the customer (Bank transfer, Credit card, electronic check, Mailed check).
19. `MonthlyCharges`: The monthly charges paid by the customer.
20. `TotalCharges`: The total charges paid by the customer to date.
21. `Churn`: Indicates whether the customer has churned (left the company) (Yes or No).

## EDA Questions:

-	Q1: How many customers we have?
-	Q2: How many have unsubscribed from our services?
-	Q3: What is the number of current customers?
-	Q4: What is the churn rate?
-	Q5: What is the average charges per month?
-	Q6: What is the annual revenue?
-	Q7: What is the sum of Monthly Charges per Internet Service?
-	Q8: What is the number of subscribed and unsubscribed customers per their demographic information?
-	Q9: What are services the subscribed and unsubscribed customers were using?
-	Q10: What is the number of subscribed and unsubscribed customers per their account information?
-	Q11: What is tenure distribution of the existing customer?
-	Q12: Which factors have the strongest correlation with churn?

## Data Cleaning:
### Exploration Summary

-	Our dataset consisted of a total of 7043 rows and 21 columns.
-	Our data is found in clean form.
-	Our dataset looks a bit tidy with no NaNs nor duplicated values.
-	`TotalCharges` column has null values that need to be handled, it has 11 nulls, and we replaced them by zero and this is done because we find tenure values equal to zero.  
-	Replaced 0 by younger and replaced 1 by older in `SeniorCitizen`.
-	Added Conditional Column `tenure category` (1:10 [Short], 11:50 [Long], >50 [Very Long])
-	No columns needed to be dropped.

## KPI Dashboard:

The KPI dashboard provides a high-level summary of critical metrics:
- **Total Customers**: 7,043
- **Churned Customers**: 1,869
- **Current Customers**: 5,174
- **Churn Rate**: 26.5%
- **Average of Monthly Charges**: 64.76
- **Annual Revenue**: $5.47M

## Conclusion
These are derived conclusions after completing our data visualisation phase.

- **Churn Rate**: The company has a churn rate of 26.5%, with 1,869 out of 7,043 customers at risk. The total annual revenue stands at $5.47M.
-	**High Churn Among Month-to-Month Contracts**: Customers on a month-to-month contract have a higher churn rate compared to those with longer-term contracts, indicating that month-to-month customers may have less loyalty.
-	**Dependents and Stability**: customers without partners or dependents have higher churn rates, highlighting a potential need for targeted retention efforts.
-	**Impact of Internet Service Type**: Customers using fiber optic internet have a higher churn rate, which could point to service quality or pricing issues with this type of connection.
-	**No Add-Ons**: Most churned customers did not subscribe to additional services like online security and tech support, suggesting that bundled services could improve retention.
-	**High-Risk Payment Methods**: Customers using electronic checks show a higher churn rate, which could suggest dissatisfaction with billing methods or payment flexibility.

## Recommendations

**Enhance Retention Among Senior Citizens**:
-	Develop loyalty programs or personalized offers targeting senior citizens to increase engagement and reduce churn in this demographic.
  
**Promote Longer-Term Contracts**:
-	Consider offering discounts or incentives for customers to switch from month-to-month to longer-term contracts. Highlight the value and savings to encourage commitment.
  
**Focus on Payment Method Options**:
-	Since electronic check users have a higher churn rate, consider educating these customers on more secure or convenient payment options like bank transfers or credit card autopay. Additionally, offering incentives for switching payment methods might improve retention.
  
**Engage Paperless Billing Customers**:
-	Introduce customer engagement programs specifically for paperless billing users. This could involve sending personalized communications, offering exclusive deals, or educating them about additional services.
  
**Optimize Service Quality for Internet Customers**:
-	Fiber optic users show a higher churn rate than DSL users. Investing in improving fiber optic service quality.
