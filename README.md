# GROCERY STORE CUSTOMER SEGMENTATION AND PURCHASE BEHAVIOUR ANALYSIS

![grocery store](https://github.com/user-attachments/assets/06d5e4c8-1f94-414b-9737-505a67acd64f)


## Introduction
As a **Quantium Job Simulation participant**, I worked on a real-world business problem that involved analyzing customer purchasing behavior for *Julia, the Chips Category Manager*. This project simulated the responsibilities of a data analyst in the retail industry, focusing on data-driven decision-making.

## Problem Statement
Julia’s goal was to understand customer segments and purchasing patterns to refine her category strategy. She is particularly interested in identifying high-value customer segments that contribute the most to revenue, understanding purchase trends, sales drivers, price sensitivity across different customer groups and develop a data-backed strategy to optimize marketing and sales efforts.

## About the Dataset

The data was provided by the Grocery Data Team and consists of two datasets:

1️⃣ Transaction Data (264,483 rows, 8 columns)

- Covers sales transactions from July 2018 to June 2019.

- Key columns: Transaction date, store number, loyalty card number, transaction ID, product number, product name, product quantity, and total sales.

2️⃣ Purchase Behavior Data (72,637 rows, 3 columns)

- Contains customer lifestage and segment classifications based on overall shopping behavior beyond chips.

- Helps in segmenting customers based on spending habits and purchase frequency.

![Screenshot 2025-03-27 202058](https://github.com/user-attachments/assets/b1f85ec7-729e-4910-aeb4-f832200cd0c8)

## Business Questions
1. What are the monthly sales trends? When is the peak month?
2. How many transactions occur per pack size, and which pack size is the most popular?
3. Which customer segment spends the most on chips? (By total revenue)
4. How many customers belong to each segment? How many chips are bought per customer in each segment?
5. What is the average price of chips per customer segment?
6. How does spending behavior differ between life stages and customer segments?

## Python Concepts Applied
While working on this project, I utilized several Python libraries for data preprocessing, analysis, and visualization:

- Pandas – Used for data manipulation, handling missing values, creating aggregated views of sales and customer segments, and merging datasets.
- NumPy – Used for numerical computations and efficient handling of large datasets.
- Regular Expressions (re) – Applied for text cleaning and pattern matching in product names or customer segments.
- Collections (Counter) – Used to analyze frequency distributions, such as identifying the most purchased chip sizes.
- Matplotlib & Seaborn – Created visualizations to analyze trends, segment-wise purchasing behavior, and seasonal sales patterns with it.
- Scipy.stats (t-test) – Conducted statistical tests (T-test) to determine significant differences between customer segments based on sales and purchasing behavior.
- Datetime – Used to extract time-based insights and analyze seasonality trends.

## Cleaning and Processing of the datasets in Python
- Changed the date data type from int to datetime.
  ![Screenshot 2025-03-27 202601](https://github.com/user-attachments/assets/a9e98652-9cea-47d0-b621-68d2a33001bf)
- We are definitely looking at potato chips but how can we check that these are all chips? I did some basic text analysis by summarising the individual words in the product name column.
  ![Screenshot 2025-03-27 203205](https://github.com/user-attachments/assets/048c9dab-3ffe-4877-bd2a-644b81b6e308)
- There are 18,094 salsa products in the dataset but we are only interested in the chips category, so I removed them.
  ![Screenshot 2025-03-28 002053](https://github.com/user-attachments/assets/fec5c4dd-acf5-4b3b-9601-45d46e5bbf02)

- Checked for the summary statistics and discovered that the product quantity has a max. of 200.
  ![Screenshot 2025-03-27 204029](https://github.com/user-attachments/assets/60c22220-a2c9-41b9-9386-30a55799fa98)
- Checked out the who the customer is

  ![Screenshot 2025-03-27 204225](https://github.com/user-attachments/assets/361bf091-e0e8-4963-848d-b573b35bad3c)
- It looks like this customer has only had the two transactions over the year and is not an ordinary retail customer. The customer might be buying chips for commercial purposes instead. 
  I removed this loyalty card number from further analysis. This means that the customer who purchased 200 packets of chips is likely not a regular retail customer but rather a business 
  customer (e.g., a restaurant, catering service, or reseller), and our analysis is focused on ordinary retail consumers.
  ![Screenshot 2025-03-27 204603](https://github.com/user-attachments/assets/4cac6b9c-d93c-4239-a32b-9e2b84d76bed)
- Counted the number of transcation per date. There are only 364 rows, meaning only 364 dates which indicates a missing date.
  ![Screenshot 2025-03-27 204744](https://github.com/user-attachments/assets/a5a9116a-76d4-4e66-9aac-ef4d7d2203b0)
- I created a sequence of dates from 1 Jul 2018 to 30 Jun 2019 and use this to create a chart of number of transactions over time to find the missing date.
  My output indicates that there are three missing dates in the transaction dataset: (July 1, 2018, July 2, 2018, December 27, 2018)
  What This Means? No transactions were recorded on these dates. This could be due to missing data, system downtimes, or actual store closures.
  ![Screenshot 2025-03-27 204958](https://github.com/user-attachments/assets/df64446c-8e86-4fce-be68-f16bca32479b)
- Extracted size of packages and brand name from product name column
  ![Screenshot 2025-03-27 205852](https://github.com/user-attachments/assets/0d0310d1-78b4-42b6-b060-4232ee1f6ba9)
- Standardized the brand name column

  ![Screenshot 2025-03-27 210152](https://github.com/user-attachments/assets/e7bbf29b-c9de-4d10-8221-bf307d431555)
- Now, that the transaction dataset is ready for analysis, I merged the two datsets and checked if the number of rows remains the same
  ![Screenshot 2025-03-27 211212](https://github.com/user-attachments/assets/2ca27ef3-1888-4019-92a0-395509770fcb)

- Then, saved my merged data into a CSV file

  ![Screenshot 2025-03-27 210504](https://github.com/user-attachments/assets/669998b9-f6cc-41e7-96ad-aaff6b42702b)

## Visualization
  ![image](https://github.com/user-attachments/assets/74c844bb-8d0e-4293-9bdb-06bc3f8eb196)
  ![image](https://github.com/user-attachments/assets/c21ca6e5-d786-4351-88d6-5edb1d755d60)
  ![image](https://github.com/user-attachments/assets/e8f95458-415e-4358-893d-269f62c1d32b)
  ![image](https://github.com/user-attachments/assets/5725772f-c81e-45c4-ac2d-01258dbc6272)
  ![image](https://github.com/user-attachments/assets/30004a2b-a28c-433a-aab2-9aaee0ae5d1a)
  ![image](https://github.com/user-attachments/assets/db4a5ecb-898c-4fc4-8813-f30abce7266c)
  ![image](https://github.com/user-attachments/assets/776e728d-5c8a-43ab-b954-0fb6013c6213)
  ![image](https://github.com/user-attachments/assets/4c296838-7cc4-481b-8b87-47195016c374)
  ![image](https://github.com/user-attachments/assets/fea3c961-8e45-40eb-80d8-84f9aac9fd5d)

## Findings
- The number of transactions was fairly steady throughout the year, with only small ups and downs. However, there were two points— one in July 2018 and another in December 2018 where 
  transactions suddenly dropped to almost zero. This is linked to the three missing dates we found earlier, possibly due to missing data, system issues, or store closures.
- Zoomed in the transcation for December 2018 because there was a steady increase in purchases in December and a break in late December. Also noticed a big jump in sales as Christmas 
  approaches and on Christmas Day itself.
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


























  







