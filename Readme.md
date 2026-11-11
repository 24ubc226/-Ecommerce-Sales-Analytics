# 📊 E-Commerce Sales & Business Intelligence Dashboard

An interactive **E-Commerce Sales and Business Intelligence Dashboard** developed using Microsoft Power BI and the Brazilian E-Commerce Public Dataset by Olist.

This project transforms real-world e-commerce data into meaningful business insights through interactive dashboards, data modelling, DAX calculations and visual analytics.

---

## 📌 Project Overview

The objective of this project is to analyse e-commerce business performance across sales, customers, payments and delivery operations.

Using Power BI, multiple datasets were cleaned, transformed and connected to build an interactive four-page dashboard that helps understand business performance and identify important trends.

## 🎯 Business Objectives

- Analyse overall sales and revenue performance.
- Identify top-performing product categories.
- Understand monthly sales trends.
- Analyse customer distribution across states.
- Evaluate payment methods and customer reviews.
- Monitor order statuses and delivery performance.
- Support data-driven business decisions.

## 📂 Dataset Information

**Dataset:** Brazilian E-Commerce Public Dataset by Olist

**Source:** Kaggle

The dataset contains anonymised real-world Brazilian e-commerce transaction data covering approximately 100,000 orders from 2016 to 2018.

### Dataset Tables

The project uses the following CSV files:

| Dataset | Description |
|---|---|
| Orders | Order details and timestamps |
| Order Items | Products purchased and transaction prices |
| Customers | Customer information and locations |
| Products | Product details and categories |
| Category Translation | Portuguese-to-English category names |
| Payments | Payment methods and transaction values |
| Reviews | Customer review scores and feedback |
| Sellers | Seller information |
| Geolocation | Geographic location information |

## 🛠️ Technologies Used

- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- Data Cleaning and Transformation
- Data Modelling
- Interactive Data Visualization
- CSV Dataset

## 📊 Dashboard Pages

The dashboard consists of four interactive analytical pages.

### 1. Executive Overview

Provides a high-level summary of overall business performance.

**Key Performance Indicators:**
- Total Revenue
- Total Orders
- Total Customers
- Average Order Value
- Average Review Score

**Visualizations:**
- Monthly Revenue Trend
- Top 10 Product Categories by Revenue
- Top 10 States by Revenue
- Payment Transactions by Type
- Orders by Status

### 2. Sales Analysis

Focuses on sales performance and revenue distribution.

**Key Performance Indicators:**
- Total Revenue
- Total Orders
- Average Order Value

**Visualizations:**
- Revenue by Product Category
- Monthly Revenue Trend
- Revenue by State

**Interactive Filters:**
- Year
- Customer State

### 3. Customer & Payment Analysis

Provides insights into customer distribution, payment behaviour and customer satisfaction.

**Key Performance Indicators:**
- Total Customers
- Average Review Score
- Payment Transactions

**Visualizations:**
- Payment Transactions by Payment Method
- Customers by State
- Review Score Distribution
- Payment Transactions by Installments

### 4. Delivery & Operations Analysis

Evaluates order fulfilment and delivery performance.

**Key Performance Indicators:**
- Delivered Orders
- Cancelled Orders
- Delivery Success Rate

**Visualizations:**
- Orders by Status
- Order Delivery Time Distribution
- Average Delivery Days by State
- Monthly Order Volume

## 📐 Data Analysis & DAX Measures

DAX measures were created to calculate important business metrics.

**Total Revenue**
```dax
Total Revenue =
SUMX(
    OrderItems,
    OrderItems[price] + OrderItems[freight_value]
)
```

**Total Orders**
```dax
Total Orders =
DISTINCTCOUNT(Orders[order_id])
```

**Total Customers**
```dax
Total Customers =
DISTINCTCOUNT(Customers[customer_unique_id])
```

**Average Order Value**
```dax
Average Order Value =
DIVIDE(
    [Total Revenue],
    [Total Orders],
    0
)
```

**Delivered Orders**
```dax
Delivered Orders =
CALCULATE(
    [Total Orders],
    Orders[order_status] = "delivered"
)
```

**Cancelled Orders**
```dax
Cancelled Orders =
CALCULATE(
    [Total Orders],
    Orders[order_status] = "canceled"
)
```

**Delivery Success Rate**
```dax
Delivery Success Rate =
DIVIDE(
    [Delivered Orders],
    [Total Orders],
    0
)
```

## 🔄 Project Workflow

1. Dataset collection and exploration.
2. Importing CSV files into Power BI.
3. Data cleaning and transformation using Power Query.
4. Handling missing values and correcting data types.
5. Creating relationships between datasets.
6. Developing a Date Table for time-based analysis.
7. Creating calculated columns and DAX measures.
8. Designing interactive dashboard pages.
9. Analysing business performance through visualizations.

## 💡 Key Learning Outcomes

Through this project, I gained practical experience in:

- Working with real-world relational datasets.
- Data cleaning and transformation using Power Query.
- Building data models and table relationships.
- Writing DAX measures for business KPIs.
- Developing interactive Power BI dashboards.
- Analysing sales, customer and operational data.
- Presenting business information through visual storytelling.

## 📁 Project Structure

```text
Ecommerce-Sales-Analytics/
│
├── README.md
│
├── Dashboard/
│   └── Ecommerce-Sales-Analytics.pbix
│
├── Screenshots/
│   ├── Executive-Overview.png
│   ├── Sales-Analysis.png
│   ├── Customer-Payment-Analysis.png
│   └── Delivery-Operations-Analysis.png
│
└── Dataset/
    └── Dataset-Source.txt
```

## 🚀 How to Use

1. Clone or download this repository.
2. Download the Brazilian E-Commerce Public Dataset by Olist from Kaggle.
3. Extract the CSV files.
4. Open the `.pbix` file using Microsoft Power BI Desktop.
5. If necessary, update the data source paths to match your local dataset folder.
6. Refresh the data to explore the dashboard.

## 📌 Future Improvements

- Add advanced customer segmentation.
- Develop customer retention and repeat-purchase analysis.
- Introduce sales forecasting.
- Explore customer churn prediction.
- Integrate additional machine learning techniques.

## 👩‍💻 Author

**Bijil Biju**

BCA (Honours) – Artificial Intelligence & Machine Learning  
Marian College Kuttikkanam Autonomous

**Areas of Interest:**
- Data Analytics
- Business Intelligence
- Artificial Intelligence
- Machine Learning

**GitHub:** 24ubc226

---

⭐ If you find this project interesting, feel free to explore the repository!
