# Project Title – Hospitality Revenue Dashboard

## 📌 Overview

This project presents an interactive Power BI dashboard designed to analyze customer churn behavior and identify key patterns across demographics, services, and subscription characteristics. The dashboard supports customer retention strategies by highlighting the most influential factors contributing to churn.

![customer churn](https://github.com/user-attachments/assets/6979f42c-5446-4798-93d3-4c83a09b1351) 

---

## 🧩 Problem Statement

Customer churn poses a significant challenge to subscription-based businesses, directly impacting revenue and long-term growth. Despite acquiring new customers, high churn rates can erode profitability and hinder customer lifetime value. The lack of visibility into why customers leave—whether due to service dissatisfaction, competitive offers, or contractual issues—limits the organization's ability to take proactive retention measures.

This project aims to analyze historical customer data using an interactive Power BI dashboard to:

- Identify key drivers of customer churn across demographics, geography, services, and subscription types.

- Detect high-risk customer segments.

- Predict potential churners for timely intervention.

By visualizing and interpreting these insights, the dashboard supports data-driven decision-making to reduce churn and enhance customer retention strategies
---

## 📊 Tools & Technologies Used

- SQL
- Power BI 
- Python (Pandas, NumPy, Matplotlib)
- Excel
- Git & GitHub

---

## 📁 Dataset

Used Customer Churn dataset from Kaggle containing:
1. Demographic Information:
  - Customer_ID: Unique identifier for each customer
  - Gender: Male / Female
  - Age Group: Binned into < 20, 20–35, 36–50, > 50
  - Marital_Status: Yes / No
  - State: Customer’s geographic location
2. Account & Contract Information:
  - Tenure: Grouped into ranges (e.g., < 6 Months, 6-12 Months, >= 24 Months)
  - Contract: Type of contract — Month-to-Month, One Year, Two Year
  - Payment_Method: Mode of payment — Credit Card, Bank Withdrawal, Mailed Check
3. Service Subscriptions:
  -Internet_Service: Yes / No
  - Internet_Type: DSL, Cable, Fiber Optic, None
  - Phone_Service: Yes / No
  - Multiple_Lines, Streaming_Movies, Streaming_Music, Online_Backup, Online_Security, Device_Protection_Plan, Premium_Support: Binary indicators showing whether a customer uses the service
4. Financial Metrics:
  - Monthly_Charge: Amount charged per month
  - Total_Revenue: Total amount paid
  - Total_Refunds: Total amount refunded
  - Number_of_Referrals: Number of people referred by the customer
5. Churn Indicators:
  - Total_Churn: Whether the customer has churned
  - Churn_Rate: Percentage of churned customers in various segments
  - Churn_Category: Reason for churn — e.g., Competitor offer, Pricing, Attitude
  - Churn_Reason: More detailed explanation of why a customer churned
6. Prediction Features
- Derived segments for prediction such as:
- Churn likelihood by age, tenure, contract type, payment method
- Count of predicted churners based on historical patterns

---

## 🧠 Approach

This churn analysis project follows a multi-tool pipeline involving SQL, Power BI, Excel, and Python for a complete data analysis and prediction solution.

1. Data Cleaning & View Creation (SQL)
- Performed data cleaning, preprocessing, and transformation using SQL.
- Addressed:
  - Missing values
  - Data type conversions
  - Standardization of categorical fields

- Created SQL views for key entities such as:
- Customer Demographics
  - Churn Status
- These views formed a clean, structured base for downstream analysis.

2. Data Visualization & Exploration (Power BI)
- Connected Power BI directly to the SQL query.
- Built dynamic visualizations to explore churn patterns:
  - **Churn rate by age, tenure, service type, and geography**
  - **KPI cards** for total customers, churned customers, churn rate
  - Service-level analysis to identify high-risk features (e.g., lack of online security or premium support)

3. Intermediate Analysis (Excel)
- Connected Excel directly to the SQL views.
-Exported cleansed and visualized data to Excel for:
  - Additional exploration
  - Preparation for machine learning modeling
- Excel served as a bridge between Power BI output and Python input.

4. Churn Prediction Modeling (Python)
- Imported the preprocessed dataset from Excel into Python.
- Applied machine learning algorithms (e.g., logistic regression, decision trees) to predict customer churn.
- Identified **important features** influencing churn:
  - Contract type
  - Monthly charge
  - Tenure
  - Services subscribed
- Generated a list of **predicted churners** with probability scores.

5. Prediction Dashboard (Power BI)
- Re-imported Python-generated churn predictions into Power BI.
- Created a **prediction-focused dashboard**:
  - Highlighting customers at risk
  - Segmentation by churn likelihood
- Visualization of predicted churn by state, tenure, and service usage
- Empowered business stakeholders to take **data-driven retention actions**.

---
## 🌟 Screenshot

![Screenshot 2025-05-12 003936](https://github.com/user-attachments/assets/785fe3dc-f286-4c26-b122-0972e450a482)

---

## 🌟 Key Features

🛠️ 1. Data Cleaning & Preparation (SQL)
- Structured customer and service data into clean SQL views
- Handled missing values, standardized formats, and removed duplicates
- Created derived fields like:
  - Tenure_Group, Age_Group, and Contract_Type
  - Binary indicators for service subscriptions

📊 2. Interactive Dashboards (Power BI)
- KPI Tiles for:
  -Total Customers
  - Total Churned
  -Churn Rate
  -New Joiners

- Drill-down Visuals by:
  - Age Group, Gender, State
  - Contract Type, Tenure, Payment Method
- Service Usage (e.g., Streaming, Backup, Security)

- Column and bar charts showing:
  - Churn rate by geography and service type
  - Top churn reasons and churn categories

📁 3. Data Integration Layer (Excel)
- Used Excel to:
- Combine cleaned SQL view outputs
- Format data for ML model input
- Perform light statistical summaries and pivoting

🤖 4. Churn Prediction Engine (Python)
- Machine Learning-based churn classification using:
  - Logistic Regression / Decision Trees / Random Forest
- Feature importance analysis
- Generated:
  - Predicted churn labels
  - Churn probabilities
- Segmented customers into High, Medium, and Low Risk

📉 5. Prediction Dashboard (Power BI)
- Visualized ML output from Python:
  - Highlighted customers likely to churn
  - Risk profile charts by tenure, contract, and geography
  - Churn risk filters (age, gender, services, charges)
- Actionable insights panel for business users to focus on retention campaigns

---

## 🏁 Results

🔍 Key Insights
- Total Customers: 6,418
- New Joiners: 411
- Total Churned Customers: 1,732
- Churn Rate: 27.0%

📈 Churn Breakdown
- By Age Group
  - Highest churn observed in the 20-35 group (31.6%)
- By Payment Method
  - Mailed Checks and Bank Withdrawals showed higher churn (37.8%, 34.4%)
  - Credit Card users had the lowest churn (14.8%)
- By Contract Type
  - Monthly contracts had a significantly higher churn rate (46.5%)
  - Two-year contracts saw minimal churn (2.7%)
- By Tenure
  - Churn rate was consistent across tenure groups (~26%-28%)
- By Geography
  - States like Jammu & Kashmir (57.2%) and Assam (38.1%) showed the highest churn
- By Internet Type
  - Fiber Optic users experienced the highest churn (41.1%)
- Users with no internet service had the lowest churn (7.8%)

🧠 Churn Prediction
- Total Predicted Churners: 385
- High churn prediction associated with:
  - Short tenures (<6 months)
  - Monthly contracts
  - Credit card payments
  - Younger customers (<35 years)
    
💼 Service-Based Churn
- Customers without:
  - Online Security (84.6%)
  - Premium Support (83.5%)
  - Device Protection (71.0%)
were more likely to churn.

🧑 Demographics
- Gender:
  - 64.15% of churned customers were female
- Marital Status:
  - Nearly even split between married and unmarried customers

---

## 📚 Learnings

- **Data integration** across SQL, Power BI, Excel, and Python enhances analytical depth and automation.

- **Monthly contracts and short tenures** are strong indicators of customer churn.

- **Service adoption** (e.g., online security, device protection) significantly impacts retention.

- **Geographic and demographic segmentation** reveals targeted opportunities for churn reduction.

- **Predictive modeling** empowers proactive churn prevention rather than reactive analysis.

- **Visual storytelling in Power BI** makes complex churn patterns easy to interpret for business users.

---
