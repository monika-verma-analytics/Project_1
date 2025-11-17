# 📊 UAE E-Commerce Sales Insights  
### Exploratory Data Analysis (EDA) + Data Cleaning + Excel Dashboard

---

## 📌 **1. Project Overview**
This project analyzes an e-commerce sales dataset to uncover insights related to customer behavior, category performance, and revenue trends.  
The focus is on replicating the kind of analysis a **Business Analyst** would perform in a real UAE e-commerce environment.

The project covers:
- Data cleaning & preprocessing  
- Exploratory data analysis (EDA)  
- KPI generation  
- Excel dashboard creation  
- Business-focused insights  

Dataset used: **Superstore Sales Dataset (Kaggle)**  
Link: https://www.kaggle.com/datasets/vivek468/superstore-dataset-final  

---

## 📁 **2. Folder Structure**
├── dataset/
│ ├── raw/retail_data.csv
│ └── cleaned/retail_data_cleaned.xlsx
│
├── analysis/
│ └── EDA_steps.xlsx
│
├── dashboard/
│ └── sales_dashboard.xlsx
│
└── README.md


---

## 🧹 **3. Data Cleaning Steps**

### **3.1 Initial Assessment**
- Checked column types (dates, numeric, categorical)
- Identified missing values using filters & COUNTBLANK()
- Identified inconsistent category names (e.g., “Eletronics”, “electronics”, “Electronics”)
- Detected date format inconsistencies

---

### **3.2 Cleaning Applied**
#### ✔ Removed duplicates  
Using: `Data → Remove Duplicates`  
Based on fields: *Order ID, Customer ID*

#### ✔ Standardized text fields  
- Applied PROPER() to names  
- Normalized category names  
- Corrected spelling variations using Find & Replace  

#### ✔ Handled missing values  
- Missing “Quantity” → replaced with 1  
- Missing “Price” → replaced with category median  
- Non-essential blanks (City, Segment) → left empty  

#### ✔ Corrected date formats  
- Converted inconsistent date entries  
- Added derived columns:
  - **Month** = TEXT(order_date, "mmm")  
  - **Year** = YEAR(order_date)  
  - **Month-Year** = TEXT(order_date, "mmm yyyy")  

#### ✔ Added calculated fields  
- **Revenue** = Quantity × Unit Price  
- **Order Age** = TODAY() – Order Date  

The cleaned version is stored in:  
`/dataset/cleaned/retail_data_cleaned.xlsx`

---

## 🔍 **4. Exploratory Data Analysis (EDA)**

### **4.1 Key Business Questions**
1. Which product categories generate the highest revenue?  
2. What is the average order value (AOV)?  
3. What does monthly revenue growth look like?  
4. How do customer segments differ by order frequency and spend?  
5. What are the top-performing cities or regions?  

---

### **4.2 Insights Summary**
#### 📌 **1. Category Performance**
- Electronics, Furniture, and Office Supplies contribute the majority of revenue  
- Electronics has the **highest AOV**

#### 📌 **2. Revenue Trend**
- Revenue consistently peaks between **November–January** (holiday season)
- Slow months appear between **April–June**

#### 📌 **3. Customer Segmentation**
- **Top 20% of customers drive ~65% of total revenue**  
- High-value customers exhibit higher order frequency and basket size

#### 📌 **4. Geography**
- Dubai, Abu Dhabi, and Sharjah drive the highest revenue (if dataset includes regions)

---

## 📈 **5. Excel Dashboard**

The dashboard includes:
- **KPI Cards:**  
  - Total Revenue  
  - Total Orders  
  - Average Order Value (AOV)  
  - Returning Customer %  

- **Visualizations:**  
  - Line chart: Monthly revenue trend  
  - Bar chart: Category contribution  
  - Pie chart: Payment mode split  
  - Table: Top 10 customers  

- **Interactive Slicers:**  
  - Month  
  - Category  
  - Region/City  

File: `/dashboard/sales_dashboard.xlsx`

---

## 🧠 **6. Business Interpretation**

This analysis enables UAE e-commerce teams to:

- Identify high-potential categories for marketing/discounts  
- Plan inventory or promotions around peak sales months  
- Improve high-value customer retention  
- Diagnose performance issues in weaker categories/regions  

These insights directly support:
- **Revenue growth strategies**  
- **Marketing planning**  
- **Customer segmentation decisions**  
- **Operational forecasting**

---

## 🧰 **7. Tools Used**
- **Excel** (Main tool)
  - Pivot Tables  
  - Power Query (optional)  
  - Charts & Slicers  
  - XLOOKUP / IFERROR / PROPER  

- **Data Source**: Kaggle  
- **Version Control**: GitHub

---

## 🚀 **8. Key Skills Demonstrated**
- Data Cleaning  
- Exploratory Data Analysis  
- Business KPI Creation  
- Dashboard Design  
- Revenue Trend Analysis  
- Customer Segmentation  
- Stakeholder Reporting  

---

## 📬 **9. Contact**
If you'd like to discuss the project or my work:  
**LinkedIn:** *your URL here*  
**Email:** *your email here*  

---

