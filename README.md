# CREDIT_CARD_FINANCIAL_DATA

### Project Brief – Credit Card Dashboard

This project focuses on analyzing credit card transactions and customer behavior using Power BI. The dashboard provides a 360° view of both transaction-level insights (Page 2) and customer-level insights (Page 3), enabling better decision-making for financial institutions.

#### The goal was to identify:

Revenue drivers across expenditure types, card categories, and payment modes.

Customer demographics and job profiles contributing the most to profitability.

Patterns in age, education, and loan adoption that impact credit card usage.

Week-on-week and quarter-on-quarter revenue trends for performance tracking.

#### To achieve this, the project integrates SQL, Power Query, and DAX:

SQL was used to extract and preprocess raw transaction data from multiple relational tables.

Power Query handled cleaning, shaping, and joining datasets (ETL pipeline).

DAX powered advanced calculations (KPIs, growth rates, satisfaction index, etc.) for interactive visualizations.

#### The final dashboard provides actionable insights for:

Business teams → targeting profitable customer segments.

Risk teams → understanding delinquency patterns.

Marketing teams → designing offers for specific demographics and expenditure categories.


### How I Used DAX, SQL & Power Query
#### 🔹 SQL

Data Extraction & Preprocessing:

Pulled raw transaction data, customer demographics, and card details from SQL tables.

Used SQL joins to combine transaction, customer, and card category tables.

Applied aggregation queries (e.g., SUM(transaction_amount), COUNT(transaction_id)) to pre-calculate revenue and transaction metrics.

#### 🔹 Power Query (ETL in Power BI)

Data Cleaning & Transformation:

Removed duplicates, handled missing values, and standardized formats (e.g., converting dates into Year-Month format).

Created a date dimension table and merged it with the fact table for time-series analysis.

Derived custom columns such as age group (20–30, 30–40, etc.), education categories, and transaction type.

#### 🔹 DAX (Measures & Calculated Columns)

Built advanced calculations for dashboard KPIs:

Revenue Growth WoW:
```dax
WoW_perc= 
DIVIDE([Current Week Revenue] - [Previous Week Revenue], [Previous Week Revenue])

```
Total Revenue, Transaction Count, and Interest Earned as dynamic measures.

Slicers & Filters: DAX was used to ensure metrics respond interactively when filtering by job type, education, expenditure, card category, or chip usage.

Customer Satisfaction Index was aggregated as an average from ratings column.

👉 This combination of SQL for backend data prep, Power Query for transformation, and DAX for analytics made the dashboard both accurate and interactive, enabling deep insights into customer and transaction behaviors.


### 📊 Insights from Page 2 – Credit Card Transaction Report

#### Quarterly Trends:

Revenue peaked in Q2 with over 0.4M, accompanied by the highest number of transactions (3201).

Q1 and Q3 showed lower performance, highlighting possible seasonal impacts on spending.

Expenditure Type:

Highest revenue came from Entertainment and Fuel (~0.26M each), while Food and Grocery contributed less.

This indicates credit card users prefer cards for lifestyle and travel-related spending rather than daily essentials.

#### Customer Segmentation:

Businessmen and Self-employed contributed the largest shares (~0.31M and ~0.28M).

Graduates generated the maximum revenue (~0.48M) compared to post-graduate and doctorate customers.

#### Card Category & Usage:

Blue cards dominated with 1.05M revenue and the majority of transaction volume.

Swipe transactions (0.75M) far outweighed Chip (0.37M) and Online (0.08M), indicating a preference for POS payments.

#### Profitability:

Interest earned was highest from Blue card users (118K), showing strong profitability from the largest customer base.

### 📊 Insights from Page 3 – Credit Card Customer Report

#### Customer Profile:

Total customer income analyzed: 12M.

Average customer age is 46, with strong engagement in the 30–50 age bracket (0.88M revenue combined).

#### Demographics & Gender Split:

Male customers contributed slightly more revenue than females.

Customers with personal loans are distributed more towards Blue card users (92%), highlighting cross-sell opportunities.

#### Revenue by Age Group:

40–50 age group leads with 0.45M revenue, followed by 50–60 group (0.43M).

Younger customers (<30) have the lowest contribution, indicating untapped growth potential.

#### Customer Satisfaction:

Average satisfaction score is 3.5, suggesting room for improvement in services and benefits.
