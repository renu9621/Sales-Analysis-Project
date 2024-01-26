# Sales-Analysis-Project

## Table of Contents

- [Project Overview](#project-overview)
- [Data Cleaning/Preparation](#data-cleaning/preparation)
- [Recommendations](#recommendations)
- [Data Analysis](#data-analysis)
- [Data Visualization](#data-visualization)
- [Insights](insigts)
  
### Project Overview

This data analysis project aims to provide insights into the sales performance of a pizza selling company over the past year. By analyzing various aspects of the sales data, we seek to identify trends, make data-driven recommendations, and gain a deeper understanding of the company's performance.

### Data Cleaning/Preparation

In the initial data preparation phase, we performed the following tasks:
Data loading: dataset is a csv file.
Data inspection

### Exploratory Data Analysis

Exploring the sales data to answer key questions, such as:

- Daily trend for total orders
- Monthly trend for total orders
- Percentage of sales by pizza category
- Percentage of sales by pizza size
- Total pizza sold by pizza category
- Top five best and worst seller by revenue, total quantity and total order

### Data Analysis

SQL queries were fired into MS SQL Server to analyse data and get resulst for problem qustions. The same result was captured and documented to cross check later.

```sql
SELECT SUM(total_price) AS Total_Revenue
FROM pizza_sales;
```
### Data Visualization

Step 1 : New measure was created to find total revenue.

Following DAX expression was written for the same,
        
        Total Revenue = SUM(pizza_sold[total_price])
        
A card visual was used to represent total revenue.

![Total revenue](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/764efa3a-da44-4f0a-8da3-fcc0067f3cf6)

Step 2 : New measure was created to find total number of orders.

Following DAX expression was written for the same,
        
        Total Orders = DISTINCT COUNT(pizza_sold[order_id])
        
A card visual was used to represent total revenue.

![Total orders](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/119f0ace-f42e-4485-bd18-d2cb0673130c)

Step 3 : New measure was created to find average order value.

Following DAX expression was written for the same,
        
        Avg Order Value = [Total Revenue]/[Total Orders]
        
A card visual was used to represent total revenue.

![Avg order value](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/4affda2b-9d7f-4d8b-b706-1a409b941e15)

Step 5 : New measure was created to find total pizzas sold.

Following DAX expression was written for the same,
        
        Total Pizzas sold = [Total Revenue]/[Total Orders]
        
A card visual was used to represent total revenue.

![total pizza sold](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/deb515f1-55ac-47ba-bfed-26b263e265c9)

Step 5 : New measure was created to find average pizzas per order.

Following DAX expression was written for the same,
        
        Avg Pizzas Per Order = [Total Pizza Sold]/[Total Orders]
        
A card visual was used to represent total revenue.

![Avg pizza per order](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/63c4083f-4067-4210-a9cb-789cd89faf7b)

Step 6 : A bar chart was created to display daily trend for total orders over a secific time period to identify any patterns or fluctuations in order.

Step 7 : A line chart was created to illustrate the peak months when the orders were maximum to identify the peak time of the year.

Step 8 : A pie chart was created to show the distribution of sales across different pizza category, which provides insight into the popularity of various pizza categories and their contributions to overall sales.

Step 9 : A pie chart was generated to represent the percentage of sales attributed to different pizza sizes. This helps us understand customer preferences for pizza sizes and their impact on sales.

Step 10 : A funnel chart was created to demonstrate the number of pizzas sold for each pizza category to compare the sales performance of different pizza categories.

Step 11 : A bar chart highlighting the top five best selling pizza based on the revenue, total quantity and total order was created to identify most popular pizza options.

Step 12 : A bar chart showcasing the bottom five worst selling pizzas based on the revenue, total quantity and total orders was created to identify underperforming or less popular pizza options.

![best_worst_seller](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/b267a345-22e6-4482-9a28-6499feb5e3c3)
![home_tab](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/b38936dd-8d72-494f-bb1d-ece9e8c74306)

### Insights

The analysis results are summarized as follows:

1. Orders were highest on weekends, Fridays/Saturdays and maximum orders were from the month of January and July.
2. Classic category contributes to maximum sales and total orders whereas large size pizza contributes to maximum sales.
3. The Thai chicken pizza contibutes to maximum revenue whereas classic deluxe pizza contributes to maximum total quantity and total orders.
4. The Brie Carre Pizza contributes to minimum revenue, toal quantity and total orders.



