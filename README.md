# 📡 Telecom Churn Analysis

---

## 📌 1. Introduction and Project Context
This project aimed to analyze customer churn in telecommunications by combining SQL Server for data preparation, Power BI for visualization, and Python for predictive modeling. It demonstrates the ability to manage the full data pipeline and deliver insights to support retention strategies.

### 🔍 Problems to Address

- High customer churn rates negatively impacting revenue and business stability.
- Lack of tools and analysis to identify and understand churn drivers.
- Data inconsistency and missing values making it difficult to build predictive models.
- No interactive dashboards to support management in making timely, data-driven decisions.
### 🎯 Analysis Objectives

- Clean and standardize telecom customer data to ensure high data quality for analysis and modeling.
- Identify key factors influencing customer churn to provide actionable insights for senior management.
- Segment customers by risk level to enable targeted retention strategies.
- Develop interactive dashboards in Power BI to monitor churn metrics and customer behavior.
- Build and evaluate predictive models (Random Forest) to forecast churn likelihood and support data-driven decision-making.

![Flowchart](https://github.com/LyraData/Churn-Analysis/blob/main/churn.png)

---

## 📂 2. Data Description

| Column                       | Description                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Customer_ID                  | A unique identifier for each customer (e.g., "19877-DEL").                                                                                                |
| Gender                       | Customer’s gender (Male or Female).                                                                                                                       |
| Age                          | Customer’s age in years.                                                                                                                                  |
| Married                      | Marital status (Yes or No).                                                                                                                               |
| State                        | The state or region where the customer resides (e.g., Delhi, Maharashtra).                                                                                |
| Number_of_Referrals          | Number of customers referred by the individual.                                                                                                           |
| Tenure_in_Months             | Duration of service usage in months.                                                                                                                      |
| Value_Deal                   | Type of promotional deal (e.g., Deal 1, Deal 5; blank if none).                                                                                           |
| Phone_Service                | Indicates if the customer uses phone services (Yes or No).                                                                                                |
| Multiple_Lines               | Indicates if the customer uses multiple phone lines (Yes, No, or blank if no phone service).                                                              |
| Internet_Service             | Indicates if the customer uses internet services (Yes or No).                                                                                             |
| Internet_Type                | Type of internet connection (Cable, Fiber Optic, DSL, or blank if no internet).                                                                           |
| Online_Security              | Indicates if the customer has online security services (Yes, No, or blank if no internet).                                                                |
| Online_Backup                | Indicates if the customer has online backup services (Yes, No, or blank if no internet).                                                                  |
| Device_Protection_Plan       | Indicates if the customer has a device protection plan (Yes, No, or blank if no internet).                                                                |
| Premium_Support              | Indicates if the customer uses premium support (Yes, No, or blank if no internet).                                                                        |
| Streaming_TV                 | Indicates if the customer uses TV streaming (Yes, No, or blank if no internet).                                                                           |
| Streaming_Movies             | Indicates if the customer uses movie streaming (Yes, No, or blank if no internet).                                                                        |
| Streaming_Music              | Indicates if the customer uses music streaming (Yes, No, or blank if no internet).                                                                        |
| Unlimited_Data               | Indicates if the customer has an unlimited data plan (Yes or No).                                                                                         |
| Contract                     | Type of contract (Month-to-Month, One Year, Two Year).                                                                                                    |
| Paperless_Billing            | Indicates if the customer uses paperless billing (Yes or No).                                                                                             |
| Payment_Method               | Payment method (Credit Card, Bank Withdrawal, Mailed Check).                                                                                              |
| Monthly_Charge               | Monthly fee (can be negative if refunds apply).                                                                                                           |
| Total_Charges                | Total amount paid by the customer.                                                                                                                        |
| Total_Refunds                | Total amount refunded to the customer.                                                                                                                    |
| Total_Extra_Data_Charges     | Total additional charges for extra data.                                                                                                                  |
| Total_Long_Distance_Charges  | Total charges for long-distance calls.                                                                                                                    |
| Total_Revenue                | Total revenue generated from the customer.                                                                                                                |
| Customer_Status              | Current status of the customer (Stayed, Churned, Joined).                                                                                                 |
| Churn_Category               | Category of churn reason (Competitor, Dissatisfaction, Price, Attitude, Other, or blank if no churn).                                                     |
| Churn_Reason                 | Specific reason for churn (e.g., "Competitor had better devices," "Price too high," or blank if no churn).                                                |


---

## ⚙️ 3. Project Implementation Steps

### 🔹 Step 1: Data Import and Cleaning
- **Objective**: Import data into SQL Server to validate unique values handle missing entries replace nulls and ensure consistency  
- **Tools**: SQL Server  
- **Results**: Clean and reliable dataset ready for analysis and modeling

### Step 2: Data Transformation and Visualization

[Click here to view demo](https://app.powerbi.com/view?r=eyJrIjoiMzZmYTBiMmMtZTNiNS00ODI4LTkwNzItNDg3ZDEzMDUxZDBjIiwidCI6ImQ2ZDEzZTBlLTdjYTAtNDNkNC05OTY1LTQyZDM4ZWU1M2RkYSIsImMiOjEwfQ%3D%3D)
- **Objective**: Query data from SQL Server into Power BI, create age and tenure groups, handle outliers, and calculate key metrics such as total customers and churn rate  
- **Tools**: Power BI, DAX  
- **Results**: Interactive dashboards displaying customer distribution, churn trends, and revenue metrics


### 🔹 Step 3: Churn Prediction Modeling
- **Objective**: Connect SQL Server data to Python clean and encode variables split into training and testing sets train a Random Forest model and generate churn predictions  
- **Tools**: Python (Pandas, scikit-learn), Jupyter Notebook  
- **Results**: Predictive model identifying high-risk customers with actionable insights

### 🔹 Step 4: Reporting and Business Insights
- **Objective**: Consolidate analysis results and present key findings to inform churn reduction strategies  
- **Tools**: SQL Server, Power BI, Python  
- **Results**: Comprehensive report and recommendations supporting customer retention efforts
---

## 🧭 4. Strategic Actions

- **Retention Campaigns:** Launch targeted discounts and promotions to encourage customers to switch from month-to-month contracts to longer-term agreements focusing especially on Fiber Optic users; run regional retention campaigns prioritizing Jammu & Kashmir and Uttar Pradesh where churn rates are highest.
- **Service Improvements:** Enhance technical support for Fiber Optic services and expand device protection offerings to increase perceived value; promptly resolve negative billing issues to rebuild customer trust.
- **Personalized Offers:** Design tailored packages for customers aged 20–50 including streaming bundles or security add-ons to better match their needs; promote credit card payments by offering incentives or reward programs.
- **Proactive Monitoring:** Closely monitor customers with 12–18 months of tenure to detect early signs of churn risk; integrate churn prediction outputs into customer care workflows to proactively reach out before contract renewals.

---

## 📊 5. Conclusion

The **Telecom Customer Churn Analysis** project enabled me to complete a full data analysis workflow—from data preparation and visualization to predictive modeling and strategic recommendations.

- Successfully processed and standardized large datasets in SQL Server, ensuring high accuracy and reliability across all analysis phases.
- Developed advanced, interactive Power BI dashboards to help management monitor churn rates, customer behavior, and revenue metrics in real time.
- Built and evaluated a Random Forest prediction model in Python to identify high-risk customers with actionable insights.
- Enhanced skills in data cleaning, transformation, modeling, and model validation.
- Effectively connected technical analysis with business goals, translating findings into concrete strategies such as personalized offers by age, long-term contract incentives, and improved technical support.
- Strengthened reporting and data storytelling abilities, delivering clear, data-driven insights to support timely decision-making.

Overall, this project not only delivered tangible business value but also demonstrated my ability to work flexibly across multiple tools (**SQL Server**, **Power BI**, **Python**) and apply analytical thinking to drive strategic outcomes.

---

