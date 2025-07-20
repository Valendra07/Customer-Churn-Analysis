# Customer-Churn-Analysis
📉 Customer Churn Analysis

A complete end-to-end data science project to analyze and predict customer churn using SQL Server, Power BI, and Python. This solution covers ETL, dashboarding, exploratory data analysis, and predictive modeling.
🚀 Project Overview

Customer churn is a major concern for subscription-based businesses. This project identifies key churn drivers and predicts customer behavior to help stakeholders take proactive measures.
✅ Key Objectives:

    Clean and preprocess churn-related data from a relational database

    Analyze churn patterns and business KPIs

    Build machine learning models to predict churn

    Deliver actionable insights through interactive dashboards

🧰 Tech Stack
Component	Tools & Libraries
Database	SQL Server
Data Analysis	Python (pandas, matplotlib, seaborn)
Dashboarding	Power BI
Machine Learning	scikit-learn, xgboost, imbalanced-learn
Notebook	Jupyter
🔄 Workflow
1. ETL and Data Preparation (SQL Server)

    Removed duplicates and handled NULL values

    Normalized column types

    Created SQL Views for easier downstream consumption

2. Exploratory Data Analysis (Python)

    Analyzed customer behavior using:

        Histograms 

        Boxplots 

        Heatmaps 

3. Handling Imbalanced Data

    Used SMOTE for oversampling minority class

    Applied Label Encoding for categorical variables

4. Model Building

    Models trained:

        Decision Tree

        Random Forest

        XGBoost

    Evaluation Metrics:

        Accuracy: 78%

        Precision (Non-Churners): 85%

        Macro F1-Score: 72%

5. Dashboarding (Power BI)

    Created interactive dashboards showing:

        Total Customers vs. Churned Customers

        Monthly Churn Rate

        Customer Segmentation by Service Usage and Contract Type

        KPIs: Total Churn, Churn Rate, Tenure Distribution

📊 Sample Visuals

Summary Page
<p align="center">
  <img src="Image/Summary_Page.png" alt="Program Flow" width="600">
</p>

Prediction Page
<p align="center">
  <img src="Image/Prediction_Page.png" alt="Program Flow" width="600">
</p>



📈 Results

    Identified top churn predictors: Contract Type, Tenure, and Monthly Charges

    Built a predictive model pipeline ready for deployment

    Delivered insights that can inform customer retention strategies
