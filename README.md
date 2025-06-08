# Chips Sales & Customer Behavior Analytics

![grocery store](https://github.com/user-attachments/assets/06d5e4c8-1f94-414b-9737-505a67acd64f)

## Introduction
I worked on a business problem that involved analyzing customer purchasing behavior for the Chips category manager of a grocery store. This project demonstrated the responsibilities of a data analyst in the retail industry, focusing on data-driven decision making. I used Python libraries for data cleaning, preprocessing, and manipulation, and leveraged Power BI to create interactive visualizations that uncovered actionable insights for strategic planning.

## Problem Statement
The goal of the chips category manager was to understand customer segments and purchasing patterns to refine her category strategy. She is particularly interested in identifying high-value customer segments that contribute the most to revenue, understanding purchase trends, sales drivers, price sensitivity across different customer groups and develop a data-backed strategy to optimize marketing and sales efforts.

## About the Dataset

The data was provided by the Grocery Data Team and consists of two datasets:

1️. Transaction Data (264,483 rows, 8 columns)

- Covers sales transactions from July 2018 to June 2019.
- Key columns: Transaction date, store number, loyalty card number, transaction ID, product number, product name, product quantity, and total sales.

2️. Purchase Behavior Data (72,637 rows, 3 columns)

- Contains customer lifestage and segment classifications based on overall shopping behavior beyond chips.
- Helps in segmenting customers based on spending habits and purchase frequency.


## Business Questions

1. What are the monthly sales trends? When is the peak month?
2. How many transactions occur per pack size, and which brand and pack size are the most popular?
3. Which customer segment spends the most on chips? (By total revenue)
4. How many customers belong to each segment? How many chips are bought per customer in each segment?
5. What is the average price of chips per customer segment?
6. How does spending behavior differ between life stages and customer segments?

## Python Concepts Applied

While working on this project, I utilized several Python libraries and concepts for data preprocessing, analysis, and visualization:

- **Data Type Conversion**: Converted the date column from integer format to datetime to enable proper time-based analysis.
- "**Text Analysis**: Performed basic text analysis on the product_name column to validate that all products fall under the chips category.
- **Category Filtering**: Identified and removed 18,094 salsa products to focus solely on the chips category.
- **Descriptive Statistics**: Analyzed summary statistics and found an unusually high maximum quantity of 200 units in the product_quantity column.
- **Customer Segmentation**: Investigated individual customer behavior and found a customer with only two bulk transactions over the year. This customer (identified via loyalty card 
                             number) was excluded from the analysis as they were likely a commercial buyer rather than a typical retail consumer.
- **Transaction Date Check**: Counted transactions per date and discovered only 364 unique dates, indicating missing records.
- **Date Sequence Generation**: Generated a complete sequence of dates from July 1, 2018, to June 30, 2019, to visualize gaps in transaction records. Identified three missing dates: 
                                July 1, July 2, and December 27, 2018 due to store closures.
- **Feature Engineering**: Extracted pack_size and brand_name from the product_name column using string operations.
- **Data Standardization**: Cleaned and standardized the brand_name column to ensure consistency in brand-level analysis.
- **Data Export for Visualization**: Saved the final cleaned dataset as a CSV file using to_csv() to prepare it for further analysis and interactive visualization in Power BI.

## Power BI Concepts Applied

- **Data Modeling**: Relationship mapping between transactions, customers, and products to support multi-level slicing.
- **DAX Measures**: Used extensively to calculate KPIs like Average Spend, Revenue per Transaction, Previous Month Variance.
- **Time Intelligence**: Implemented for comparing metrics across months (e.g., % change vs. previous month).
- **Interactive Filters**: Slicers for customer segment, brand, pack size, and month allow dynamic filtering of visuals.
- **Custom Tooltips & Formatting**: Enhanced readability and interactivity with dynamic colors, conditional formatting, and formatted KPI cards.
- **Drill-Down Navigation**: Page separation between "Sales & Pricing" and "Customer Insights" for focused storytelling.

## Dashboard Breakdown [Interact with dashboard here](https://app.powerbi.com/view?r=eyJrIjoiNzBkNTIxMmEtNzI2ZC00NGVhLWE5N2EtYjdiZGUxMjU2ZTNiIiwidCI6Ijc3ZGJjZTk5LTYwNTQtNGFiYS04MjUwLTE5YzBlZmI0MzE4ZCJ9)

### Page 1: Sales & Pricing
- **Key Metrics:** Total Revenue($2M), Quantity(471K), Avg. Price per Pack($3.84), Avg. Revenue per Transaction($7.37).
- **Visuals:** Monthly Revenue Trend, Avg. Price per Customer Segment, Revenue by Customer Segment, Brands and Pack Size.
- **Insights Delivered:** Performance trends over time, High-value customer segments, Top brands and pack sizes contributing to sales.

### Page 2: Customer Insights
- **Key Metrics:** Total Customers(73K), Transactions(245k), Avg. Spend per Customer($25.34), Avg. Daily Order(674).
- **Visuals:** Daily Order Trend, Customer Segmentation, Customer Purchase Behaviour, Customer Spending Habit.
- **Insights Delivered:** Behavior trends across life stages and segments, Purchase frequency and volume insights, Segment-level value analysis.

## Findings

- The number of transactions was fairly steady throughout the year, with only small ups and downs. However, the peak months are December 2019 and March 2019, with a total sales of 
  $156.470 and $156,052 consecutively.
- Out of the 245k transactions that occured throughout the year, Kettle brand appeared 41k times making it the most popular brand. Other brands like Doritos, Smiths, Pringles, Infuzion, 
  RRD, Sunbites, Thins and WW are also doing well.
- 175 grams pack size have the highest number of transactions (66k), while other pack sizes have significantly fewer transactions. Meanwhile, not all the brands produce the 175g pack 
  size. So, the 
- Sales generally are coming mainly from Budget - older families, Mainstream - young singles/couples, and Mainstream - retirees.
- Highest number of customers are from Mainstream - Young singles/couples, and Mainstream - Retirees, while the fewer New families generally are our customers.
- Older families on budget and Mainstream- Young Singles/Couples buy more chips per customer.
- Mainstream - young singles/couples and midage are more willing to pay more per packet of chips compared to their budget and premium counterparts, Premium new families are also more willing to pay more per packet of chips compared to their budget and mainstream counterparts.

## Summary and Recommendations
- Our most valuable customer base are Mainstream - Young Singles/Couples.
- Since the Mainstream segment makes up the largest portion of our customer base, marketing efforts should be focused on them.
- To maximize sales, prioritize production, promotions, and restocking of the popluar brands and pack size.
- Since Mainstream mid-age and young singles/couples are willing to pay more per packet, introduce unique flavors, organic or healthier ingredient to appeal to those who are not 
  specifically looking for healthy snack alternatives.

![2025](https://github.com/user-attachments/assets/e2ee72cb-acce-427f-a7b2-709e6e63131f)


























  







