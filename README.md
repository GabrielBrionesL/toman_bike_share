# Recommendation Summary for Price Increase at Toman Bike Shop

---

## Key Insights from Data Analysis:

### 1. Peak Sales Hours:
- Highest sales occur between **10 AM and 3 PM** on weekdays.
- **Wednesday** and **Friday** show significant spikes.
- These times and days are the most profitable, suggesting opportunities for optimized pricing and resource allocation.

### 2. Revenue and Profit Growth:
- **Revenue doubled** from $4.96M in 2021 to $10.23M in 2022 following a price increase from **$3.99 to $4.99**.
- **Profit increased by 105%**, growing from $3.42M to $7.03M, showing that demand was not negatively impacted by the price increase.
- **Revenue per rider** grew in line with the price increase, directly boosting total revenue.

### 3. Demand Elasticity:
- A **25% price increase** in 2022 resulted in a **65% increase** in riders, indicating **elastic demand**.
- Customers are tolerating higher prices, supporting another moderate increase.

### 4. Seasonality and Rider Type:
- **Season 3** (likely summer) generated the most revenue at **$4.9M**, making it the best time for a price adjustment.
- **Registered riders** (81.17%) form a loyal customer base, likely to be less price-sensitive compared to casual riders.

---

## Recommendations:

### 1. Implement a Moderate Price Increase:
- Recommend raising the average price per rider by **$0.50 to $1.00** starting in **Season 3** to capture higher demand during peak periods without reducing rider volume.

### 2. Optimize Operational Resources:
- Focus on optimizing staffing and promotions during **10 AM to 3 PM** on high-traffic days (Wednesday, Friday) to maximize profitability.

### 3. Monitor Customer Response:
- Track rider behavior after the price increase, especially among **casual riders** (18.83%) to ensure no significant drop-off among price-sensitive customers.

### 4. Leverage Registered Riders:
- Consider **personalized offers** or loyalty incentives to retain the large base of **registered riders**, while encouraging premium services or memberships.

---

## Methodology:

To analyze the data, we queried historical bike share records stored in SQL Server. The query combined data from two different tables representing different years of bike-share data and performed calculations to derive metrics such as revenue and profit. Here is the SQL query used:

## Explanation:
- **CTE (Common Table Expression)**: The CTE merges data from two tables (bike_share_yr_0 and bike_share_yr_1) representing different years of bike share operations.
- **Revenue Calculation**: For each entry, we calculated revenue as riders * price, where riders is the number of customers for a particular time and price is the price per rider.
- **Profit Calculation**: Profit was calculated by subtracting the total cost of goods sold (COGS) from the revenue. This was derived as riders * price - (COGS * riders).
- **Seasonality and Hourly Data**: The query captures data points like season, weekday, and hour (hr), allowing us to identify peak sales times and the impact of seasonality on revenue and profit.

This methodology allowed us to calculate key metrics like revenue, profit, and cost, giving us the necessary data to make informed recommendations on pricing strategies.

---

## Expected Impact:
- **Revenue Growth**: projected to increase by 5-10% next year.
- **Profit Margin**: Expected to remain stable or increase with the new price point.

## Further Considerations:
While this analysis provides clear recommendations for a moderate price increase, there are additional factors that could be explored with a data science project:
- **Price Elasticity Modeling**: Using more advanced techniques like regression analysis or machine learning to build a model that predicts customer response to price changes. This could help identify the optimal price point that maximizes revenue while minimizing rider churn.
- **Customer Segmentation**: A clustering algorithm could be used to segment riders based on price sensitivity, ride frequency, and other behaviors. This would allow for more targeted pricing strategies for different customer groups (e.g., registered vs. casual riders).
- **Time Series Forecasting**: A more advanced time series forecasting model could be used to predict future rider volumes and revenue based on historical trends, seasonality, and external factors. This would help refine the timing and magnitude of future price changes.
- **External Factor Analysis**: Incorporating external data, such as economic indicators, weather conditions, and competitor pricing, to further understand how these variables impact rider behavior and the effectiveness of price increases.
