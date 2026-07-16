

# Customer Analytics & Segmentation for an Online Retail Business
<p align="center">
    <img src="image/work-flow.png" width="700">
</p>

# **1. Executive Summary**  

This project analyzes customer purchasing behavior using **Exploratory Data Analysis (EDA), Cohort Analysis, and RFM Segmentation** on the Online Retail dataset.

The objective is to identify high-value customers, measure customer retention, understand purchasing patterns, and uncover revenue growth opportunities.

The analysis reveals three key business insights:

- Customer retention declines significantly after the first purchase.
- Purchasing behavior is highly seasonal, with demand concentrated during the holiday period.
- A relatively small group of loyal customers generates the majority of customer value.

Based on these findings, the project proposes data-driven CRM strategies to improve customer retention, increase Customer Lifetime Value (CLV), and optimize marketing investment.     

# **2. Business Problem**

The company has accumulated a large volume of transactional data but lacks a clear understanding of customer purchasing behavior and long-term customer value. Without customer segmentation and retention analysis, it is difficult to identify high-value customers, improve marketing effectiveness, and develop targeted CRM strategies.This project addresses these challenges by analyzing customer transactions to uncover purchasing patterns, evaluate customer retention, segment customers based on RFM, and provide data-driven recommendations for improving customer loyalty and maximizing revenue.

**Business Questions**

- Who are the most valuable customers?
- Which customer segments generate the highest revenue?
- How well are customers retained over time?
- Which customer cohorts show the strongest loyalty?
- How can customer segmentation support more effective CRM strategies?

# **3. Data Understanding**

## **About this file**
This dataset was collected and made available by Dr. Daqing Chen, Director of Public Analytics Group at the School of Engineering and Mathematical Sciences, City University, London. It was contributed to the UCI Machine Learning Repository in December 2010.

The dataset consists of transactional data from a UK-based online retailer that mainly sells unique all-occasion gifts. The transactions span from December 1, 2010, to December 9, 2011. The data includes sales of over 500,000 transactions, reflecting product purchases made by customers in various countries, with a focus on non-store purchases.

**Key Features:**
- InvoiceNo: The invoice number associated with the transaction. A numeric identifier for each transaction.
- StockCode: The code of the purchased product. A unique identifier for each product.
- Description: A brief description of the product.
- Quantity: The quantity of each product purchased per transaction.
- InvoiceDate: The date and time when the transaction was generated.
- UnitPrice: The unit price of the product.
- CustomerID: A unique identifier for the customer.
- Country: The country from which the customer made the purchase.

**Purpose and Usage:**
This dataset can be utilized for a variety of purposes, including but not limited to:
- Customer Segmentation: Analyzing purchasing patterns to classify customers based on their buying behavior.
- Product Recommendation: Developing recommendation systems based on the purchase history.
- Sales Forecasting: Predicting future sales based on historical data trends.
- Market Basket Analysis: Identifying associations between products frequently bought together.

**Researchers and practitioners** can leverage this dataset to build and test machine learning models related to sales prediction, customer retention, and inventory management.

# **4. Data Preparation** 
| Task             | Description                             |
| ---------------- | --------------------------------------- |
| Missing `CustomerID` |  Removed rows with missing `CustomerID` |
| Missing `Description` | Filled missing Description values with "Unknown". |
| Duplicates       | Removed duplicate records.              |
| Invalid `Quantity` | Removed rows where `Quantity <= 0`.     |
| Invalid `Price`   | Removed rows where `UnitPrice <= 0`.    |
| Data Types       | Converted datatype from object, string to datetime, int, float, string, category    |

# **5. Feature Engineering** 
### Objective: 

>Create meaningful features to support customer behavior analysis, cohort analysis, and RFM segmentation.

| Feature                     | Formula / Description                   | Purpose                                  |
| --------------------------- | --------------------------------------- | ---------------------------------------- |
| **Revenue**                 | `Quantity × UnitPrice`                  | Calculate transaction revenue.           |
| **InvoiceMonth**            | First day of the invoice month          | Monthly sales trend and cohort analysis. |
| **CohortMonth**             | Customer's first purchase month         | Identify customer cohorts.               |
| **CohortIndex**             | Months since first purchase             | Calculate customer retention over time.  |
| **Recency**                 | Days since the customer's last purchase | Measure purchase recency.                |
| **Frequency**               | Number of unique invoices               | Measure purchase frequency.              |
| **Monetary**                | Total revenue per customer              | Measure customer lifetime spending.      |
| **RFM Score**  | Combined R, F, and M scores             | Customer segmentation.                   |
| **Segment**    | Champions, Loyal Customers, etc.        | Marketing strategy by customer group.    |

# **6. EDA**
### Objective:

The exploratory data analysis (EDA) aims to understand sales performance, customer purchasing behavior, and product trends through descriptive statistics and data visualization. This step helps identify meaningful patterns and provides a foundation for subsequent customer analytics.

### Analysis Overview: 
The following analyses were performed:

#### Sales Distribution
- Distribution of transaction revenue
- Distribution of quantity purchased
- Distribution of unit price
- Identification of outliers using box plots
#### Sales Performance
- Monthly revenue trend
- Revenue distribution by country
- Top-selling products by revenue
#### Customer Purchasing Behavior
- Distribution of Average Order Value (AOV)
- Revenue per transaction
- Purchase frequency analysis
#### Key Insights
- Revenue is highly concentrated among a small number of high-value transactions.
- Most customers place relatively small orders, while a limited number of customers generate exceptionally large purchases.
- Sales exhibit clear temporal fluctuations, indicating potential seasonal purchasing behavior.
- A small number of countries contribute the majority of total revenue, suggesting opportunities for market prioritization.
- Product sales are highly skewed, with a few best-selling products accounting for a significant share of overall revenue.

# **7. Cohort Analysis**

# **8. RFM Segmentation**

# **9. Business Recommendations**

