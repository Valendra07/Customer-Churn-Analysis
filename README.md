# Customer-Churn-Analysis

A complete end-to-end data science project to analyze customer churn data using SQL Server, Power BI and predict future churners using Machine Learning Model. This solution covers ETL in MS SQL Server, dashboarding in Power BI, exploratory data analysis using Python libraries and predictive modeling by implementing and choosing the best one among three models: 
1. XGBClassifier
2. Random Forest Classifier
3. Decision Tree Classifier


🚀 Project Overview

Customer churn is a major concern in Telecom Industry. This project analyse the customer data to find key reasons leading to customer churn using Summary Report, predict future churners and then analyse the churner profile using Prediction report.

✅ Key Objectives:

Project Goals:

The primary objective is : 
1. To Create an entire ETL (Extract, Transform, Load) process in a database & a Power BI dashboard to effectively utilize Customer Data and achieve the following: 
Analyze Customer Data at below levels:

a. Demographic (e.g., age, gender)
b. Geographic (e.g., state)
c. Payment & Account Info (e.g., contract type, payment method, tenure)
d. Services (e.g., internet service, phone service, streaming)

2. Study Churner Profile & Identify Areas for Implementing Marketing Campaigns (e.g., understanding reasons for churn and targeting at-risk customers).

3. Using ML Model to Predict Future Churners.

Metrics Used:
To measure the success and analyze churn, the following key metrics are essential: 
Total Customers.
Total Churn : Number of lost customers.
Churn Rate : The percentage of customers who have left the Telecom Company Service.
New Joiners : number of newly acquired customers.
 
🧰 Tech Stack
Component	Tools & Libraries
Database	: Microsoft SQL Server
Data Analysis	Python (pandas, matplotlib, seaborn)
Dashboarding	Power BI
Machine Learning	scikit-learn
Notebook Jupyter


🔄 Workflow
0. Understanding the dataset:
Here's the representation of dataset used in the project.

<p align="center">
  <img src="Image/Customer Churn Data.png" alt="Program Flow" width="600">
</p>

The 31 columns can broadly classified into 6 major categories :
   a. Cutomer ID : Unique Key
   b. Personal Information 
   c. Account Info
   d. Services Subscribed by the customer
   e. Revenue Related Columns 
   f. Customer Status : Target Column

1. ETL and Data Preparation (MS SQL Server)
    a. Database and Table Creation
    b. Removed duplicates and handled NULL values.
    c. View Creation

    ETL Framework :
   Data Source : CSV file containing data.
  Microsoft server management Studio : To transform and load data in SQL server database using import Wizard
 SQL server database : To store data, tables and views.

3. Dashboarding (Power BI)
    Loaded the data in power bi and used power query editor to create custom column called chain status and  monthly charged range.
    Created Summary Page having following measures:

      Total Customers = COUNT(Customer_Data[Customer_ID])

      Total Churn = SUM(Customer_Data[Churn Status])

      New Joiner = CALCULATE(COUNT(Customer_Data[Customer_ID]),Customer_Data[Customer_Status]="Joined")

      Churn Rate = [Total Churn]/[Total Customers]

    Prediction Page uses following measure:

      Count Predicted Churner = COUNT(Predictions[Customer_ID]) + 0
                
📊 Sample Visuals

Summary Page
<p align="center">
  <img src="Image/Summary_Page.png" alt="Program Flow" width="600">
</p>

Prediction Page
<p align="center">
  <img src="Image/Prediction_Page.png" alt="Program Flow" width="600">
</p>

Key Insights from Data Analysis (Summary Page)

    Senior Customers: Individuals aged above 60 years exhibit a notably higher churn rate compared to other age groups.

    Tenure-Based Churn: Customers with a tenure of less than 2 months are more likely to churn, in contrast to those with 1-year or 2-year commitments, who show significantly lower churn rates.

    Gender Disparity: Female customers demonstrate a higher churn rate compared to male customers.

    Service-Based Churn: Customers who have subscribed to Phone Services, Internet Service, and Unlimited Data plans exhibit a churn rate exceeding 60%.

Machine Learning Module — Customer Churn Prediction

This Jupyter notebook focuses on predicting customer churn using various machine learning algorithms. It is a core component of the larger Customer Churn Analysis project.
📌 Key Features

    Data Preprocessing:

        Removal of non-informative columns (e.g., customerID)

        Handling of missing values in TotalCharges

        Label encoding of categorical variables.

    Class Imbalance Handling:

        Applied SMOTE (Synthetic Minority Oversampling Technique) to balance churn classes

    Model Building:

        Implemented and compared:

            Decision Tree Classifier

            Random Forest Classifier

            XGBoost Classifier

    Model Evaluation:

        Accuracy Score

        Confusion Matrix

        Classification Report (Precision, Recall, F1-Score)

   Saved the csv file of predicted churners for analysis in Power BI.

📈 Results

    Built a predictive model pipeline ready for deployment

    Delivered insights that can inform customer retention strategies.
