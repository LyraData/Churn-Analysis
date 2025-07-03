# 🏠 Telecom Churn Analysis

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

![Flowchart](https://github.com/LyraData/ComeInn-Home-Analysist/blob/main/FLOWCHART.png)

---

## 📂 2. Data Description

- **BRANCHES**: Includes BranchID, Name, Address; used to manage branch information.  
- **ROOMS**: Includes RoomID, BranchID, RoomNumber, BedCount, Area, RoomType, RoomGender, Amenities; used to manage rooms and amenities.  
- **BEDS**: Includes BedID, RoomID, Position, BedNo; used to manage beds within rooms.  
- **CUSTOMERS**: Includes CustomerID, FullName, DateOfBirth, Gender, IdentityNumber, PhoneNumber, Address, Email, VehiclePlateType, VehicleType, AppRegistered, TemporaryResidenceRegistered, TempResidenceExpiryDate, Age, AgeGroup; used to store customer information.  
- **CONTRACTS**: Includes ID, CustomerID, BedID, StartDate, EndDate, CheckoutDate, Status, IsRenewal, ContractLength; used to manage rental contracts.  
- **PRICE**: Includes PriceID, BedID, Price, ElectricityPrice_per_kWh, WaterPrice_per_person, ParkingFee_per_vehicle; used to manage room pricing and service fees.  

---

## ⚙️ 3. Project Implementation Steps

### 🔹 Step 1: Data Cleaning and Standardization (Python)
- **Objective**: Standardize data from `combined_customers.csv` (238 records).  
- **Tools**: Python (Pandas, NumPy, Seaborn, Matplotlib), Jupyter Notebook.  
- **Results**: Cleaned data, age analysis (56% aged 18–24), app registration status (58% unregistered), age group distribution visualized via bar charts.

### 🔹 Step 2: SQL Queries for Data Analysis (T-SQL)
- **Objective**: Extract detailed insights for management decision-making.  
- **Tools**: SQL (JOIN, CTE, Window Functions).  
- **Results**: 50+ queries for revenue analysis, loyal customer identification, vacancy rates, and anomaly detection.

### 🔹 Step 3: Power BI Dashboard
- **Objective**: Visualize revenue, customer, and operational performance.  
- **Results**: 4B VND revenue, 78% occupancy rate, dormitories (KTX) contribute 66.2% of revenue, identified high/low demand seasons and high-churn branch.

### 🔹 Step 4: Machine Learning Analysis
- **Objective**: Predict churn, segment customers, analyze time-to-churn and pricing.  
- **Results**:  
  - **Churn Prediction**: ROC AUC 0.78, key factor (ActualStayDays).  
  - **Segmentation**: 3 clusters (loyal females, new customers, high-income males).  
  - **Time-to-Churn**: Long contracts and renewals reduce churn risk.  
  - **Time Series**: Prices fluctuate by day/week.  
  - **Amenity Recommendation**: Personalized amenity suggestions.  
  - **A/B Testing**: 5–10% price increase does not affect renewal rates.

### 🔹 Step 5: Flask API Deployment
- **Objective**: Predict churn and recommend suitable rooms.  
- **Results**: API with 70–80% accuracy, automates churn prediction and room allocation.

---

## 🧭 4. Strategic Actions

1. **Stabilize Seasonal Revenue**: Offer summer discounts, boost marketing in peak months, and forecast Q3 revenue.  
2. **Reduce Churn**: Send payment reminders, offer installments to young tenants, and collect exit feedback.  
3. **Optimize Rooms & Amenities**: Expand KTX rooms and upgrade Wi-Fi and water quality.  
4. **Increase Contract Value**: Provide 6-month contracts with free amenities and launch a loyalty program.  
5. **Data Management**: Update dashboards monthly and forecast churn 30 days ahead.  

---

## 📊 5. Conclusion
After completing the project, I significantly expanded my skills and understanding in several key areas:
• **Used Python** for data cleaning, standardizing information from multiple sources, handling missing values, and preparing training datasets for prediction models.  
• **Wrote SQL queries** to filter, aggregate, and analyze data, such as calculating contract renewal rates, monthly revenue statistics, and identifying high-risk customer segments.  
• **Enhanced data visualization skills** with Power BI, designed interactive reports, and leveraged **DAX** to create measures and compare business metrics across time periods.  
• **Built statistical and predictive models**, strengthening my knowledge of machine learning concepts.  
• **Gained hands-on experience with Flask API**, learning how to package predictive models into automated recommendation services.  
• **Developed a deep understanding** of the student dormitory and room rental domain, including key factors affecting occupancy rates, peak revenue periods, and how to diagnose and address revenue declines.  
• Through the process of self-directed research and end-to-end implementation, I also learned how to **integrate multiple tools into a cohesive workflow** — from data preparation and analysis to forecasting and building reporting dashboards — which improved my overall **data mindset** and ability to quickly learn new technologies.

---

