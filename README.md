# 🛍️ Customer Shopping Behavior Analysis

## 📌 Project Overview

**Customer Shopping Behavior Analysis** is an end-to-end data analytics project focused on understanding customer purchasing patterns, spending behaviour, product preferences, and customer demographics.

The project uses **Python, Pandas, SQL, PostgreSQL, and Power BI** to transform raw customer data into meaningful business insights.

The analysis starts with data cleaning and exploratory data analysis in Python, continues with SQL-based business analysis, and ends with an interactive Power BI dashboard.

---

## 🎯 Business Problem

Understanding customer shopping behaviour is important for businesses to improve sales, marketing strategies, customer satisfaction, and customer retention.

This project aims to analyze customer data and answer questions such as:

* Which product categories generate the highest sales?
* What are the purchasing patterns of customers?
* Which customers have higher spending?
* How does customer age affect purchasing behaviour?
* Which categories are most popular among customers?
* What insights can help businesses improve their sales strategy?

---

## 🎯 Project Objectives

* Clean and preprocess the customer shopping dataset.
* Perform Exploratory Data Analysis (EDA) using Python.
* Analyze customer behaviour using Pandas.
* Perform business analysis using SQL.
* Work with a PostgreSQL database.
* Build an interactive Power BI dashboard.
* Identify important customer and sales trends.
* Generate actionable business insights.

---

# 🛠️ Technologies Used

| Technology          | Purpose                           |
| ------------------- | --------------------------------- |
| 🐍 Python           | Data analysis and preprocessing   |
| 🐼 Pandas           | Data cleaning and EDA             |
| 🔢 NumPy            | Numerical operations              |
| 🗄️ PostgreSQL      | Database management               |
| 💻 SQL              | Business analysis                 |
| 📊 Power BI         | Dashboard and visualization       |
| 📓 Jupyter Notebook | Python analysis                   |
| 🐙 GitHub           | Project hosting and documentation |

---

# 📂 Project Structure

```text
Customer-Shopping-Behavior-Analysis/
│
├── 📄 Business Problem Document.pdf
│
├── 📄 Customer Shopping Behavior Analysis.pdf
│
├── 📊 Customer_Behavior_Dashboard.pbix
│
├── 💻 Customer_behavior_analysis.sql
│
├── 📓 Customer_shopping_behaviour_analysis.ipynb
│
└── 📁 customer_shopping_behavior.csv
```

---

# 🔄 Project Workflow

```text
                 Raw Dataset
                      │
                      ▼
        Data Cleaning & Preprocessing
                      │
                      ▼
             Python / Pandas
                      │
                      ▼
          Exploratory Data Analysis
                      │
                      ▼
              SQL Analysis
                      │
                      ▼
              PostgreSQL
                      │
                      ▼
               Power BI
                      │
                      ▼
           Interactive Dashboard
                      │
                      ▼
             Business Insights
```

---

# 🐍 1. Python & Pandas Analysis

The `Customer_shopping_behaviour_analysis.ipynb` notebook contains the complete Python-based analysis.

Python and Pandas were used for:

* Loading the dataset
* Understanding the data
* Data cleaning
* Handling missing values
* Checking duplicate records
* Data transformation
* Exploratory Data Analysis
* Grouping and aggregation
* Customer behaviour analysis

### Example Pandas Code

```python
import pandas as pd
import numpy as np
```

### Load Dataset

```python
df = pd.read_csv("customer_shopping_behavior.csv")

df.head()
```

### Dataset Information

```python
df.info()
```

### Check Missing Values

```python
df.isnull().sum()
```

### Check Duplicate Records

```python
df.duplicated().sum()
```

### Statistical Analysis

```python
df.describe()
```

### Category Analysis

```python
df["category"].value_counts()
```

### Revenue by Category

```python
df.groupby("category")["purchase_amount"].sum().sort_values(
    ascending=False
)
```

### Average Purchase by Category

```python
df.groupby("category")["purchase_amount"].mean().sort_values(
    ascending=False
)
```

These operations were used to understand customer purchasing patterns and identify important trends in the dataset.

---

# 💻 2. SQL Analysis

The `Customer_behavior_analysis.sql` file contains SQL queries used to perform business analysis on the customer shopping data.

SQL was used to answer important business questions.

### Total Revenue

```sql
SELECT 
    SUM(purchase_amount) AS total_revenue
FROM customer_shopping_behavior;
```

### Average Purchase Amount

```sql
SELECT 
    AVG(purchase_amount) AS average_purchase_amount
FROM customer_shopping_behavior;
```

### Category-wise Revenue

```sql
SELECT 
    category,
    SUM(purchase_amount) AS total_revenue
FROM customer_shopping_behavior
GROUP BY category
ORDER BY total_revenue DESC;
```

### Customer Count by Category

```sql
SELECT 
    category,
    COUNT(*) AS customer_count
FROM customer_shopping_behavior
GROUP BY category
ORDER BY customer_count DESC;
```

### Top Customers

```sql
SELECT 
    customer_id,
    name,
    purchase_amount
FROM customer_shopping_behavior
ORDER BY purchase_amount DESC
LIMIT 10;
```

SQL analysis helped convert raw customer data into useful business information.

---

# 🗄️ 3. PostgreSQL

PostgreSQL was used as the database for storing and querying the customer shopping data.

The dataset was imported into PostgreSQL and analyzed using SQL queries.

### Database Workflow

```text
CSV Dataset
     ↓
PostgreSQL Database
     ↓
SQL Queries
     ↓
Business Insights
```

---

# 📊 4. Power BI Dashboard

The `Customer_Behavior_Dashboard.pbix` file contains the interactive Power BI dashboard.

The dashboard was created to provide a visual overview of customer shopping behaviour.

### Dashboard Features

* 📌 KPI Cards
* 💰 Revenue Analysis
* 👥 Customer Analysis
* 🛍️ Category Analysis
* 📊 Purchase Analysis
* 👤 Demographic Analysis
* 🔎 Interactive Filters
* 📈 Data Visualizations

The Power BI dashboard makes it easier to identify trends and patterns and supports data-driven business decisions.

> **Note:** `.pbix` files need to be opened using **Microsoft Power BI Desktop**.

---

# 📄 5. Business Problem Document

`Business Problem Document.pdf` contains the business problem and requirements considered during the development of this project.

It defines the business context, objectives, and analytical requirements of the project.

---

# 📄 6. Project Report

`Customer Shopping Behavior Analysis.pdf` contains the detailed documentation/report of the project.

It provides information about the analysis, methodology, findings, and project outcomes.

---

# 📁 7. Dataset

The project uses:

```text
customer_shopping_behavior.csv
```

The dataset contains customer shopping information used for:

* Customer analysis
* Purchase analysis
* Category analysis
* Demographic analysis
* Revenue analysis
* Business insights

---

# 💡 Key Business Insights

The analysis helps businesses understand:

* Customer purchasing behaviour
* Spending patterns
* Popular product categories
* Category-wise revenue performance
* Customer demographics
* High-value customers
* Purchasing trends

These insights can support better **marketing, customer retention, product planning, and sales strategies**.

---

# 📈 Business Value

This project demonstrates how raw customer data can be transformed into actionable business insights using an end-to-end analytics workflow.

### Business Benefits

✅ Better understanding of customers
✅ Identification of high-value customers
✅ Improved marketing strategies
✅ Better product and category planning
✅ Data-driven decision making
✅ Improved sales analysis
✅ Interactive business reporting

---

# 🧠 Skills Demonstrated

### Python

* Python
* Pandas
* NumPy
* Data Cleaning
* Data Preprocessing
* Exploratory Data Analysis

### SQL

* SELECT
* WHERE
* GROUP BY
* ORDER BY
* Aggregate Functions
* Business Queries

### PostgreSQL

* Database Creation
* Data Import
* SQL Querying
* Database Analysis

### Power BI

* Data Visualization
* Dashboard Development
* KPI Cards
* Charts
* Filters & Slicers
* Business Reporting

### Data Analytics

* Data Cleaning
* EDA
* Customer Behaviour Analysis
* Business Problem Solving
* Data-Driven Decision Making

---

# 🚀 How to Use This Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
```

### 2. Open the Jupyter Notebook

Open:

```text
Customer_shopping_behaviour_analysis.ipynb
```

### 3. Install Required Libraries

```bash
pip install pandas numpy sqlalchemy psycopg2-binary jupyter
```

### 4. Run the Python Analysis

Run the notebook cells sequentially to perform data cleaning and exploratory data analysis.

### 5. Perform SQL Analysis

Open:

```text
Customer_behavior_analysis.sql
```

Run the queries in PostgreSQL/pgAdmin.

### 6. Open the Power BI Dashboard

Open:

```text
Customer_Behavior_Dashboard.pbix
```

using Microsoft Power BI Desktop.

---

# 📌 Project Highlights

```text
🐍 Python + Pandas
        ↓
🧹 Data Cleaning
        ↓
📊 Exploratory Data Analysis
        ↓
💻 SQL + PostgreSQL
        ↓
📈 Power BI Dashboard
        ↓
💡 Business Insights
```

This project demonstrates a complete **end-to-end Data Analytics workflow** from raw data to business intelligence.

---

# 👩‍💻 Author

**Priyanka Pandey**

🎓 B.Tech Computer Science & Engineering
📊 Aspiring Data Analyst

### Areas of Interest

* Data Analytics
* Python
* SQL
* Power BI
* PostgreSQL
* Data Visualization
* Machine Learning

---

## ⭐ If you find this project useful

Feel free to ⭐ star the repository and explore the project files.
