🛒 Customer Shopping Behavior Analysis
An end-to-end data analytics project analyzing retail customer purchasing behavior, sales patterns, customer segmentation, discount impact, and revenue distribution. The workflow includes data extraction, cleaning, and feature engineering in Python, automated database ingestion into MySQL, advanced SQL querying, interactive reporting in Power BI, and executive presentation deck creation using Gamma.
📌 Project Overview
The main goal of this project is to analyze 3,900 customer shopping transactions to extract actionable business insights. By evaluating key metrics such as purchase amounts, discount dependency, subscription status, shipping preferences, and product review ratings, this analysis helps guide targeted marketing, loyalty program optimization, and inventory strategy.
📊 Dataset
Source: Customer Shopping Behavior Dataset (customer_shopping_behavior.csv)
Size: 3,900 Records | 18 Features
Key Columns:
Demographics: Customer ID, Age, Gender, Location
Transaction Details: Item Purchased, Category, Purchase Amount (USD), Size, Color, Season, Payment Method
Behavioral & Loyalty Attributes: Review Rating, Subscription Status, Shipping Type, Discount Applied, Previous Purchases, Frequency of Purchases
🛠️ Tech Stack & Tools
Tool / Library
Usage
Python (Pandas, NumPy)
Data Loading, EDA, Data Cleaning, Missing Value Imputation, Feature Engineering
SQLAlchemy & PyMySQL
Automated Pipeline for Database Migration (Python to MySQL)
MySQL Workbench
Relational Database Management & Business Analytical Queries
Power BI
Data Modeling, Interactive Visualization, Dashboard Design, KPI Tracking
Gamma App
Executive Presentation & Storytelling Deck Generation
GitHub
Code Version Control and Documentation
🔄 End-to-End Workflow & Steps
1. Data Processing & Cleaning (Python)
EDA & Inspection: Examined data structure, statistical summary, and missing values using Pandas (df.info(), df.describe()).
Missing Value Imputation: Handled missing values in Review Rating by replacing them with the median rating per Category.
Standardization: Converted column titles to snake_case (e.g., Purchase Amount (USD) $\rightarrow$ purchase_amount).
Feature Engineering:
Created age_group by binning age values into four quantiles: Young Adult, Adult, Middle-aged, Senior.
Mapped text frequency strings into numeric values (purchase_frequency_days).
Column Cleanup: Analyzed promo_code_used vs discount_applied, confirmed identical values, and removed redundant columns.
2. Database Migration & SQL Queries (MySQL)
Connected Python to MySQL database (customer_behavior) using SQLAlchemy.
Transferred clean Pandas DataFrames to MySQL tables automatically.
Formulated SQL scripts to answer business questions (Aggregations, Window Functions, CTEs, Case Statements, Cohort Analysis).
3. Interactive Reporting (Power BI)
Imported structured tables from MySQL into Power BI.
Calculated key DAX metrics (Total Revenue, Average Spend, Customer Counts, Rating Averages).
Formatted dynamic slicers (Category, Gender, Season) and interconnected visualizations.
4. Presentation & Insights Deck (Gamma)
Summarized core findings into a visual, executive-ready presentation deck to communicate findings with business stakeholders.
📈 Power BI Dashboard Features
KPI Metrics: Total Revenue ($233K+), Total Customers (3,900), Average Purchase Amount (~$59.76), Average Review Rating (~3.75).
Demographic Analysis: Revenue contribution across Age Groups and Gender divisions.
Product Insights: Top 5 highest rated products, discount dependence percentage per item.
Customer Loyalty Segmentation: Subscriber vs Non-subscriber revenue breakdown and repeat buyer behavior analysis.
🔍 Key Findings & Results
Revenue Distribution: Male customers generated $157,890 in revenue compared to $75,191 from female customers. The Middle-aged and Young Adult segments brought in the highest overall revenue ($62.1K and $59.1K respectively).
Shipping Preference: Express Shipping recorded slightly higher average spend ($60.48) than Standard Shipping ($58.46).
Subscriber Conversion Gap: Non-subscribers generated the vast majority of revenue ($170,436 across 2,847 customers) vs subscribers ($62,645 across 1,053 customers). Over 2,500 repeat buyers (>5 purchases) are not yet subscribed, highlighting a key conversion opportunity.
Customer Segmentation: Binned customers into 3,116 Loyal buyers, 701 Returning buyers, and 83 New buyers.
Discount Impact: 839 high-spending customers relied on discounts. Hats (50.00%) and Sneakers (49.66%) showed the highest discount sensitivity.
Product Ratings: Gloves (3.86) and Sandals (3.84) held the highest average review ratings.
💡 Business Recommendations
Targeted Subscriptions: Implement promotional pop-ups or loyalty points for non-subscribers with more than 5 previous purchases to increase subscription rates.
Revise Discount Strategies: Limit discount offerings on high-demand items (like Hats and Sneakers) to safeguard profit margins.
Marketing Focus: Direct ad spend toward Young Adults and Middle-aged cohorts who drive the largest portion of transaction volume.
Premium Shipping Bundles: Offer free Express Shipping thresholds for orders over $60 to drive higher basket sizes.
🚀 How to Run
Prerequisites
Make sure you have the following installed:
Python 3.x + Jupyter Notebook
MySQL Server & MySQL Workbench
Power BI Desktop
1. Clone Repository
git clone https://github.com/your-username/customer-shopping-behavior-analysis.git
cd customer-shopping-behavior-analysis
2. Python Environment & ETL
Install required packages:
pip install pandas pymysql sqlalchemy jupyter
Open and execute the Jupyter Notebook:
jupyter notebook customer_shopping_analysis.ipynb
(This cleans the CSV data and exports the customer table straight into your local MySQL database)
3. MySQL Queries
Open MySQL Workbench.
Load and run customer_behavior_queries.sql on the customer_behavior database to view query outputs.
4. Dashboards & Presentations
Open Power_BI_Dashboard.pbix using Power BI Desktop to interact with visualizations.
Open Presentation_Deck.pdf to review the executive slide deck.
Created as part of a Data Analytics Portfolio Project.

This `README.md` file covers all your tools (Python, MySQL, Power BI, Gamma), datasets, results, and step-by-step instructions.

### Next Steps:
1. Create a `README.md` file in your project folder on your computer or directly on GitHub.
2. Copy and paste the markdown code into your `README.md` file.
3. Replace `your-username` in the GitHub link with your actual GitHub username.

Would you like any adjustments to the metrics or specific section headings before you upload it?
