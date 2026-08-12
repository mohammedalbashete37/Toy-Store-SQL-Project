Project Overview:
This project analyzes the e-commerce performance of Toy Store using transaction and web session data sourced from Maven Analytics. The analysis evaluates core business functions including revenue growth across 2012–2015, product portfolio profitability, marketing channel conversion rates, repeat traffic behaviors, and product refund/return impact.
Business Questions:
Which products drive the vast majority of total revenue and profit margin?
How has revenue and average order revenue evolved month-over-month and year-over-year?
Which marketing acquisition channels (UTM sources) deliver the highest volume and conversion rates?
Do repeat web session visitors convert at a higher rate compared to new visitors?
What is the total refund percentage across orders, and which products generate the highest refund liabilities?

SQL Skills Used:

Aggregations & Grouping: SUM(), AVG(), COUNT(), COUNT(DISTINCT), GROUP BY, HAVING


Window Functions: ROW_NUMBER() OVER(PARTITION BY ... ORDER BY ...)


Joins: INNER JOIN, LEFT JOIN 
Conditional Logic & Data Cleaning: CASE WHEN, COALESCE(), NULLIF()


Common Table Expressions (CTEs): WITH CTE_Name AS (...) 
Type Casting & Formatting: CAST(), ROUND(), DECIMAL


Analysis & Results:
1. Overall Revenue Growth & Seasonality
Yearly Average Revenue: Average order revenue increased from $49.99 in 2012 to $63.80 in 2014, stabilizing at $62.80 in early 2015.
Peak Revenue Months: Performance steadily grew from $2,999.40 in March 2012 to a peak of $144,823.02 in December 2014. The end-of-year holiday surge (November–December) consistently drives maximum volume.
2. Product Revenue Rank & Margins
The Original Mr. Fuzzy: Dominates the portfolio across all years (2012–2015).
Total Volume: 29,618 units sold across 23,861 orders


Total Revenue: $1,419,767.87


Net Profit: $879,952.06 (Avg Selling Price: $59.50, Cost: $22.62)

Secondary Products:
The Forever Love Bear: $318,109.19 total revenue ($200,348.01 profit).
The Birthday Sugar Panda: $180,857.04 total revenue ($122,410.51 profit).
The Hudson River Mini Bear: $19,775.72 total revenue ($13,429.00 profit).

3. Revenue Classification Category:
High Revenue (> $500k): The Original Mr. Fuzzy
Medium Revenue ($100k - $500k): The Forever Love Bear, The Birthday Sugar Panda
Low Revenue (< $100k): The Hudson River Mini Bear

5. Marketing Channel Breakdown & Traffic Source Conversion:
Traffic Distribution: gsearch leads paid volume with 316,035 sessions (6% conversion rate). bsearch generated 62,823 sessions (7% conversion rate). Unknown channels accounted for 83,328 sessions.
Social Channels: socialbook drove 10,685 sessions but yielded the lowest conversion rate at 3%.

7. Session Type Behavior (New vs. Repeat):
New Visitors (is_repeat_session = 0): 6.64% conversion rate.
Repeat Visitors (is_repeat_session = 1): 7.83% conversion rate.
Repeat Visitor Traffic: Unknown sources account for 62% of repeat traffic.

9. Product Refund Analysis:
Overall Refund Rate: 5% of all unique orders incurred a refund.
Refund Values:
The Original Mr. Fuzzy: Highest absolute dollar refund ($61,837.63) due to sales volume.
The Birthday Sugar Panda: $13,842.99 refunded.
The Forever Love Bear: $7,738.71 refunded.
The Hudson River Mini Bear: $1,919.36 refunded.

Key Insights:
Product Concentration Risk: "The Original Mr. Fuzzy" accounts for over 70% of total profit. Expanding marketing focus on mid-tier products like "The Forever Love Bear" can diversify revenue risks.
Repeat Visitor Value: Repeat visitors convert at a higher rate (7.83% vs 6.64%). Retaining users and bringing them back generates higher organic value.
Marketing Efficiency: socialbook has a low 3% conversion rate and 0% repeat session contribution. Reallocating budget toward search networks (gsearch / bsearch) will maximize acquisition ROI.
