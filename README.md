# GROCERY STORE CUSTOMER SEGMENTATION AND PURCHASE BEHAVIOUR ANALYSIS

![grocery store](https://github.com/user-attachments/assets/06d5e4c8-1f94-414b-9737-505a67acd64f)


## Introduction
I worked on a real-world business problem that involved analyzing customer purchasing behavior for the Chips category manager of a grocery store. This project demonstrated the responsibilities of a data analyst in the retail industry, focusing on data-driven decision making. I used Python libraries for data cleaning, preprocessing, and manipulation, and leveraged Power BI to create interactive visualizations that uncovered actionable insights for strategic planning.

## Problem Statement
The goal of the chips category manager was to understand customer segments and purchasing patterns to refine her category strategy. She is particularly interested in identifying high-value customer segments that contribute the most to revenue, understanding purchase trends, sales drivers, price sensitivity across different customer groups and develop a data-backed strategy to optimize marketing and sales efforts.

## About the Dataset

The data was provided by the Grocery Data Team and consists of two datasets:

1️⃣ Transaction Data (264,483 rows, 8 columns)

- Covers sales transactions from July 2018 to June 2019.

- Key columns: Transaction date, store number, loyalty card number, transaction ID, product number, product name, product quantity, and total sales.

2️⃣ Purchase Behavior Data (72,637 rows, 3 columns)

- Contains customer lifestage and segment classifications based on overall shopping behavior beyond chips.

- Helps in segmenting customers based on spending habits and purchase frequency.


## Business Questions
1. What are the monthly sales trends? When is the peak month?
2. How many transactions occur per pack size, and which pack size is the most popular?
3. Which customer segment spends the most on chips? (By total revenue)
4. How many customers belong to each segment? How many chips are bought per customer in each segment?
5. What is the average price of chips per customer segment?
6. How does spending behavior differ between life stages and customer segments?

## Python Concepts Applied
While working on this project, I utilized several Python libraries for data preprocessing, analysis, and visualization:

- Data Type Conversion: Converted the date column from integer format to datetime to enable proper time-based analysis.
- Text Analysis: Performed basic text analysis on the product_name column to validate that all products fall under the chips category.
- Category Filtering: Identified and removed 18,094 salsa products to focus solely on the chips category.
- Descriptive Statistics: Analyzed summary statistics and found an unusually high maximum quantity of 200 units in the product_quantity column.
- Customer Segmentation: Investigated individual customer behavior and found a customer with only two bulk transactions over the year. This customer (identified via loyalty card number) was excluded from the analysis as they were likely a commercial buyer rather than a typical retail consumer.
- Transaction Date Check: Counted transactions per date and discovered only 364 unique dates, indicating missing records.
- Date Sequence Generation: Generated a complete sequence of dates from July 1, 2018, to June 30, 2019, to visualize gaps in transaction records. Identified three missing dates: July 1, July 2, and December 27, 2018—possibly due to store closures or data collection issues.
- Feature Engineering: Extracted package_size and brand_name from the product_name column using string operations.
- Data Standardization: Cleaned and standardized the brand_name column to ensure consistency in brand-level analysis.
- Data Export for Visualization: Saved the final cleaned dataset as a CSV file using to_csv() to prepare it for further analysis and interactive visualization in Power BI.

## 
nn

## Findings
- The number of transactions was fairly steady throughout the year, with only small ups and downs. However, there were two points— one in July 2018 and another in December 2018 where 
  transactions suddenly dropped to almost zero. This is linked to the three missing dates we found earlier, possibly due to missing data, system issues, or store closures.
- Zoomed in the transcation for December 2018 because there was a steady increase in purchases in December and a break in late December. Also noticed a big jump in sales as Christmas 
  approaches, on Christmas Day itself and Boxing day.
- 170 grams pack size have the highest number of transactions, while other pack sizes have significantly fewer transactions.
- Sales are coming mainly from Budget - older families, Mainstream - young singles/couples, and Mainstream - retirees
- Highest number of customers are from Mainstream - Young singles/couples, and Mainstream - Retirees, while the fewer New families generally are our customers.
- Older families on budget and Mainstream- Young Singles/Couples buy more chips per customer.
- Mainstream midage and young singles and couples are more willing to pay more per packet of chips compared to their budget and premium counterparts.

## Summary and Recommendations
- Our most valuable customer base are Mainstream - Young Singles/Couples. Since the Mainstream segment makes up the largest portion of our customer base, marketing efforts should be 
  focused on them.
- The Kettle brand and 175g pack size are highly preferred by our key customer segment. Additionally, the 170g pack size has the highest number of transactions. To maximize sales, 
  prioritize production, promotions, and restocking of these popular products.
- Since Mainstream mid-age and young singles/couples are willing to pay more per packet, introduce unique flavors, organic or healthier ingredient to appeal to those who are not 
  specifically looking for healthy snack alternatives.

## Further research and Analysis
Experimentation and uplift testing, comparing trial and control stores 
- Define metrics to select control store.
- Analyze trial stores against control stores.
- Summarize findings and provide recommendation.

![2025](https://github.com/user-attachments/assets/e2ee72cb-acce-427f-a7b2-709e6e63131f)


























  







