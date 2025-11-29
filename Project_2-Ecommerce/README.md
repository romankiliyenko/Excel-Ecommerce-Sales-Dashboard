# 📊 E-Commerce Sales & Customer Analytics Dashboard

## 📘 Introduction

This Excel-based interactive dashboard was developed to analyze e-commerce sales performance and customer behavior.

The dataset includes four years of transactional data, covering product categories, sales, profits, regions, customer activity, and order information.

The goal of the project is to:

- Understand key revenue & profit drivers

- Compare performance by category and region

- Identify high-value customers

- Apply **Pareto (80/20)** and **RFM segmentation** to support data-driven decisions

- Provide a clean and interactive dashboard for business insight

### 📂 Dashboard File

📄 Download the full Excel dashboard here:
[2_Ecommerce_Analysis.xlsx](2_Ecommerce_Analysis.xlsx)

### 🛠️ Excel Skills Used

The following Excel skills were applied throughout the project:

- 📉 **Charts & Data Visualization**

- 🧮 **Advanced Formulas (IFs, QUARTILE, TEXT, DATE, RFM logic)**

- 📊 **Pivot Tables & Pivot Charts**

- 🎛️ **Interactive Slicers (Region, Category, Year)**

- 🧼 **Data Cleaning & Transformation**

- 📁 **Structured Tables & Dynamic Ranges**

### 📦 Dataset Description

The dataset contains transactional e-commerce data with the following fields:

- **🛒 Product Category & Sub-Category**

- **👤 Customer Name**

- **📆 Order Date & Ship Date**

- **📍 Region**

- **💰 Sales, Profit, Quantity, Discount**

It includes **~800 customers** and **4 years (2014–2017)** of order history.


### 🧼 Data Cleaning Steps

Performed in the **Data_Cleaned** tab:

#### ✔ Date Standardization

- Converted inconsistent date formats using **Text-to-Columns**

- Ensured alignment & correctness (all left-aligned = text → fixed)

#### ✔ New Calculated Columns

```
Profit Margin  = Profit / Sales
Delivery Days  = Ship Date - Order Date
Year           = YEAR(Order Date)
Month Num      = MONTH(Order Date)
Month Name     = TEXT(Order Date, "mmm")
Quarter        = "Q" & INT((Month Num + 2)/3)
```


### 📊 Dashboard Build

#### 1️⃣ Sales, Profit & Profit Margin by Category
<img width="780" height="630" alt="Screenshot 2025-11-26 at 22 17 01" src="https://github.com/user-attachments/assets/30d67c26-2de9-45fc-9f07-450ff32bfb82" />

- **Excel Features:** Clustered column + line chart

- **Design Choice:** Dual-axis to compare Sales vs Profit Margin

- **Insights:**

   - Technology: highest revenue & strong margins

   - Furniture: weakest profit margin

   - Office Supplies: mid-sales, high margins


#### 2️⃣ Sales by Region
<img width="762" height="629" alt="Screenshot 2025-11-26 at 22 17 09" src="https://github.com/user-attachments/assets/e05ba7da-76e1-4007-9563-797f3e7d3569" />

- **Insights:**

   - West region leads revenue

   - South region underperforms

   - Strong margin differences across regions


#### 3️⃣ Monthly Sales Trend by Year

- Shows year-over-year seasonality

- Slicers allow interactive filtering by:

   - **Category**

   - **Year**

   - **Region**

💡 Significant growth observed in 2017.

### 👥 Customer Analysis

#### 4️⃣ Customer Sales Segmentation (Pareto 80/20)
<img width="701" height="595" alt="Screenshot 2025-11-26 at 22 18 42" src="https://github.com/user-attachments/assets/aaaf6bfa-fa77-4028-85b4-0b3d40a0704b" />

- Top **~20%** of sub-categories generate **~80%** of revenue

- Phones, Chairs, Storage → key drivers

- Long tail of low-performing categories

#### 5️⃣ Revenue Contribution by Customer Tier
<img width="716" height="596" alt="Screenshot 2025-11-26 at 22 18 00" src="https://github.com/user-attachments/assets/1c836043-485e-4ae8-b3af-526d068d493b" />

Customer tiers were assigned using **Pareto segmentation:**

- **A-VIP** – top 80% revenue

- **B-Medium** – next 15%

- **C-Low Value** – last 5%

**📌 VIP customers represent nearly 50% of all customers but drive ~80% of revenue.**


### 🔢 RFM Analysis (Recency, Frequency, Monetary)
#### 6️⃣ RFM Metrics Calculation
```
Recency   = Days since last purchase
Frequency = Total number of orders
Monetary  = Total spending
```

Scoring applied using:
```
=IFS(
    R >= QUARTILE.EXC(RR,3), 5,
    R >= QUARTILE.EXC(RR,2), 4,
    R >= QUARTILE.EXC(RR,1), 3,
    TRUE, 2
)
```
<img width="483" height="254" alt="Screenshot 2025-11-29 at 22 44 11" src="https://github.com/user-attachments/assets/76a50743-d67d-4270-9379-a32dbe6501fb" />

#### 7️⃣ RFM Segments Distribution
<img width="723" height="583" alt="Screenshot 2025-11-26 at 22 18 50" src="https://github.com/user-attachments/assets/814103b3-c6c7-4563-ab84-ef27277c5242" />

Segments:

- **🏆 Champions** – best customers

- **💙 Loyal** – frequent consistent buyers

- **⚠️ At Risk** – haven’t purchased recently

- **🔹 Others** – low R, F, M

💡 Champions are few but extremely profitable.
💡 At Risk customers present upsell/reactivation opportunities.

## 📈 Final Dashboard Overview

### 🧠 Key Insights Summary

- Technology is the top-performing category

- Furniture struggles with margins

- West region drives most revenue

- Sales trending upward over 4 years

- VIP customers account for a majority of revenue

- Pareto rule clearly applies to sub-categories

- RFM revealed re-engagement opportunities in At Risk segment

### 🚀 Conclusion

This Excel dashboard provides a comprehensive overview of e-commerce performance, combining product, regional, and customer analytics.
Using a mix of pivot tables, charts, calculated metrics, and segmentation models, it effectively visualizes key business insights and enables data-driven decision-making.

It demonstrates strong skills across data cleaning, visualization, analysis, and dashboard design using Excel.
