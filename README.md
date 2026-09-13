\# Retail Sales Analysis



Project Overview

This project analyzes retail transaction data to understand business performance. It covers data cleaning, exploratory analysis and visualization to answer key business questions about revenue, products, countries, and customers.



Dataset

The dataset contains 528 raw retail transactions with the following columns: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID and Country. The raw data includes some data quality issues such as duplicates, missing values, cancelled transactions and invalid entries, which are addressed during cleaning.



Tools Used

\- Python

\- pandas

\- matplotlib

\- Jupyter Notebook



Data Cleaning

The following issues were identified and handled:

\- Removed 8 exact duplicate rows

\- Removed 7 rows with missing Description (could not be recovered)

\- Filled 10 missing CustomerID values with "Unknown" to preserve valid sales while excluding them from customer-specific analysis

\- Converted InvoiceDate from text to a proper date format

\- Removed rows with negative or zero Quantity (cancelled or invalid orders)

\- Fixed 5 rows with UnitPrice of 0 by matching the correct price from the same product elsewhere in the data

\- Removed 3 extreme outlier Quantity values (5000, 7500, 9999) that appeared to be data entry errors

\- Standardized inconsistent country name capitalization (e.g. "GERMANY" vs "Germany")



The cleaned dataset was saved separately from the raw data to keep the original data intact.



Analysis Performed

\- Total revenue and number of transactions

\- Average order value

\- Top 10 products by revenue

\- Top 5 countries by revenue

\- Top 10 customers by revenue

\- Monthly revenue trend

\- Correlation between quantity and revenue

\- Additional questions: transactions by day of week and average order value by country



Key Findings

1\. The United Kingdom generates the vast majority of revenue compared to all other countries.

2\. A small number of products (POSTAGE, REGENCY CAKESTAND 3 TIER, CREAM CUPID HEARTS COAT HANGER) generate a large share of total revenue.

3\. Revenue is seasonal, peaking in July and August and dropping to its lowest in January.

4\. Most transactions are small in value, with only a few large orders.

5\. France has the highest average order value despite the UK generating the most total revenue overall.



Visualizations

The notebook includes the following charts, each with a written interpretation:

1\. Monthly revenue trend (line chart)

2\. Top 10 products by revenue (bar chart)

3\. Top 5 countries by revenue (bar chart)

4\. Distribution of transaction values (histogram)

5\. Quantity vs revenue relationship (scatter plot)



A "bad chart" example is also included, showing common visualization mistakes and how to fix them.



Recommendations

1\. Keep top-selling products well-stocked and consider promoting them further.

2\. Plan extra stock and marketing campaigns around July and August and investigate ways to boost sales during slower months like January.

3\. Explore growth opportunities in other countries, such as targeted marketing in markets like France or Australia that show higher average order values.



How to Run the Project

1\. Clone this repository

2\. Install the required packages: `pip install -r requirements.txt`

3\. Open `notebooks/retail\_sales\_analysis.ipynb` in Jupyter Notebook

4\. Run all cells from top to bottom

