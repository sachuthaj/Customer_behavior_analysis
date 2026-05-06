🛍️ Customer Shopping Behavior — End-to-End Data Analytics Project
> An end-to-end data analytics project covering data loading, exploratory analysis, SQL querying, and interactive Power BI visualization on a retail customer shopping dataset.
---
📌 Overview
This project analyzes the shopping behavior of 3,900 retail customers across the United States. The goal is to uncover patterns in purchasing habits, customer segments, product performance, and revenue trends — simulating a real-world business analytics workflow from raw data to executive-ready dashboards.
The project follows a complete analytics pipeline:
```
Raw CSV → Python (EDA & Cleaning) → SQL Queries → CSV Exports → Power BI Dashboard → Report & Presentation
```
---
📂 Dataset
Source: `customer_shopping_behavior.csv`
Size: 3,900 rows × 18 columns
Column	Description
Customer ID	Unique identifier for each customer
Age	Customer age (18–70)
Gender	Male / Female
Item Purchased	Product name (25 unique items)
Category	Clothing, Footwear, Accessories, Outerwear
Purchase Amount (USD)	Transaction value ($20–$100)
Location	US state (50 states)
Size	S / M / L / XL
Color	Product color (25 variants)
Season	Spring / Summer / Fall / Winter
Review Rating	Customer rating (2.5–5.0)
Subscription Status	Yes / No
Shipping Type	Standard, Express, Free Shipping, etc.
Discount Applied	Yes / No
Promo Code Used	Yes / No
Previous Purchases	Number of prior transactions (1–50)
Payment Method	Credit Card, PayPal, Venmo, Cash, etc.
Frequency of Purchases	Weekly, Fortnightly, Monthly, Annually, etc.
---
🛠️ Tools & Technologies
Tool	Purpose
Python (Pandas)	Data loading, EDA, cleaning
Google Colab	Development environment
SQLite (`sqlite3`)	SQL query execution on the dataset
SQL	Business queries and aggregations
Power BI	Interactive dashboard and visualization
Gamma	AI-powered presentation creation
GitHub	Version control and project sharing
---
🔢 Steps
1. Data Loading
Loaded `customer_shopping_behavior.csv` using `pandas`
Inspected dataset shape, column types, and sample rows with `df.head()` and `df.describe()`
2. Exploratory Data Analysis (EDA)
Checked for missing values and data types
Generated descriptive statistics for numerical columns (Age, Purchase Amount, Review Rating, Previous Purchases)
Identified distributions across categorical fields (Gender, Category, Season, Payment Method)
3. Data Cleaning
Standardized column names to lowercase with underscores for SQL compatibility
Created a derived `age_group` column:
Young Adult (18–25), Adult (26–40), Middle Aged (41–55), Senior (56+)
Loaded the cleaned DataFrame into an in-memory SQLite database for querying
4. SQL Analysis
Wrote and executed 10 business SQL queries covering:
#	Query	Key Insight
Q1	Total revenue by product category	Clothing & Accessories lead in sales
Q2	Average purchase amount by gender	Comparable spend across genders
Q3	Top 5 states by total revenue	High-revenue geographic markets
Q4	Most popular payment methods	Credit Card, PayPal, Venmo dominate
Q5	Seasonal revenue trends	Identifies peak shopping seasons
Q6	Top 5 products by discount rate	Hat, Sneakers, Coat most discounted
Q7	Customer segmentation	3,116 Loyal · 701 Returning · 83 New
Q8	Top 3 products per category	Using `ROW_NUMBER()` window function
Q9	Repeat buyers vs subscription status	Most repeat buyers are non-subscribers
Q10	Revenue by age group	Young Adults generate the most revenue
Each query result was exported as a separate `.csv` file for use in Power BI.
5. Power BI Dashboard
Imported all 10 query output CSVs into Power BI Desktop
Built an interactive dashboard with slicers, bar charts, pie charts, and KPI cards
Visuals cover revenue by category, customer segments, seasonal trends, and payment behavior
6. Report & Presentation
Report: Written analysis summarizing key findings, methodology, and business recommendations
Presentation: Created using Gamma — AI-generated slides with visuals and storytelling structure
---
📊 Dashboard
> Power BI dashboard covers the following views:
Revenue breakdown by category and season
Customer segmentation (New / Returning / Loyal)
Top products and discount leaders
Geographic revenue distribution by US state
Payment method and shipping preference analysis
📎 Dashboard `.pbix` file and screenshots available in the `/dashboard` folder.
---
📈 Key Results
Young Adults (18–25) are the highest revenue-generating segment at $62,143
80%+ of customers fall into the "Loyal" segment (10+ previous purchases)
Hat has the highest discount rate at 50%, followed by Sneakers and Coat
Jewelry is the top-selling Accessories product; Pants leads in Clothing
Most repeat buyers (2,518 out of 3,476) do not hold a subscription — a potential upsell opportunity
---
🚀 How to Run
Prerequisites
```
Python 3.x
pandas
sqlite3 (built-in)
Google Colab or Jupyter Notebook
Power BI Desktop (Windows)
```
Steps
1. Clone the repository
```bash
git clone https://github.com/your-username/customer-shopping-behavior-analysis.git
cd customer-shopping-behavior-analysis
```
2. Run the notebook
Open `Customer_behavior_sql_queries.ipynb` in Google Colab or Jupyter
Upload `customer_shopping_behavior.csv` when prompted
Run all cells sequentially — this will perform EDA, load data into SQLite, run all 10 queries, and export CSVs
3. Open the Power BI dashboard
Open `dashboard/Customer_Behavior_Dashboard.pbix` in Power BI Desktop
Refresh data sources if prompted, pointing to the exported CSV files
4. View the report and presentation
Report: `/report/Customer_Behavior_Analysis_Report.pdf`
Presentation: `/presentation/Customer_Behavior_Presentation.pdf` (or Gamma link)
---
📁 Project Structure
```
customer-shopping-behavior-analysis/
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── notebook/
│   └── Customer_behavior_sql_queries.ipynb
│
├── sql_outputs/
│   ├── q1_revenue_by_category.csv
│   ├── q2_avg_purchase_by_gender.csv
│   ├── q3_top_states_revenue.csv
│   ├── q4_payment_methods.csv
│   ├── q5_seasonal_revenue.csv
│   ├── q6_discount_rate.csv
│   ├── q7_customer_segments.csv
│   ├── q8_top_products_per_category.csv
│   ├── q9_repeat_buyers.csv
│   └── q10_revenue_by_age_group.csv
│
├── dashboard/
│   └── Customer_Behavior_Dashboard.pbix
│
├── report/
│   └── Customer_Behavior_Analysis_Report.pdf
│
├── presentation/
│   └── Customer_Behavior_Presentation.pdf
│
└── README.md
```
---
👤 Author
Sachutha
B.Sc. Computer Science & Statistics — Kristu Jayanti College, Bengaluru
📧 sachuthaj@gmail.com · 🔗 LinkedIn · 💻 GitHub
---
> *This project was built as part of a data analytics portfolio to demonstrate end-to-end skills across Python, SQL, and business intelligence tools.*# Customer_behavior_analysis
Dataanalytics project showcasing customer behavior analysis using python , sql and power bi
