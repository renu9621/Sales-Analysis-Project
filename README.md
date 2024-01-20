# Sales-Analysis-Project

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Recommendations](#recommendations)

### Project Overview

This data analysis project aims to provide insights into the sales performance of a pizza selling company over the past year. By analyzing various aspects of the sales data, we seek to identify trends, make data-driven recommendations, and gain a deeper understanding of the company's performance.

### Data Sources

Sales Data: The primary dataset used for this analysis is the "pizza_sales.csv" file, containing detailed information about each sale made by the company.

### Tools

- My SQL - Data Analysis
- PowerBI - Data Cleaning and Creating reports

### Data Cleaning/Preparation

In the initial data preparation phase, we performed the following tasks:
Data loading and inspection.
Handling missing values.
Data cleaning and formatting.

### Exploratory Data Analysis

Exploring the sales data to answer key questions, such as:

- Daily trend for total orders
- Monthly trend for total orders
- Percentage of sales by pizza category
- Percentage of sales by pizza size
- Total pizza sold by pizza category
- Top five best and worst seller by revenue, total quantity and total order

### Data Analysis

Include some interesting code/features worked with

```sql
SELECT * FROM table1
WHERE cond = 2;
```
### Steps followed
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

![Daily_trend](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/ad1aa269-2d82-408b-ae8f-e9b1d3b3c7a2)

Step 7 : A line chart was created to illustrate 

![line_chart](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/1ba2fdba-1f0c-4744-be6e-6543df8cc927)

Step 8 : A pie chart was created to show the distribution of sales across different pizza category, which provides insight into the popularity of various pizza categories and their contributions to overall sales.

![pie_chart1](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/3fdcdbc4-4099-407a-9e4a-2ea12d55eb60)

Step 9 : A pie chart was generated to represent the percentage of sales attributed to different pizza sizes. This helps us understand customer preferences for pizza sizes and their impact on sales.

![pie_chart2](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/e4054a90-8889-4162-a719-9ed33151944c)

Step 10 : A funnel chart was created to demonstrate the number of pizzas sold for each pizza category to compare the sales performance of different pizza categories.

![funnel_chart](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/ccc9d337-e60a-49c5-883d-6e664373562e)

Step 11 : A bar chart highlighting the top five best selling pizza based on the revenue, total quantity and total order was created to identify most popular pizza options.

![best_seller](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/a8e46946-b802-48d3-9db0-7b15ea0700e0)

Step 12 : A bar chart showcasing the bottom five worst selling pizzas based on the revenue, total quantity and total orders was created to identify underperforming or less popular pizza options.

![worst_seller](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/5db153f1-a20d-493d-916f-e2fb3ceedec6)

### Results/Findings

The analysis results are summarized as follows:
1. The company's sales hve been teadily increasing over the past year, with a noticeable peak duing the holiday season.
2. Product category A is the best performing ctegory in terms of sal and revenue.
3. Customer segments with high lifetime value (LTV) should be targeted for marketing efforts.

### Recommendations

Based on the analysis, we recommend the following actions:
- Invest in marketing and promotions during peak sales season to maximize revenue.
- Focus on expanding and promoting products in Category A.
- Implement a customer segmentation strategy to target high-LTV customers effectively.

### Limitations

I had to remove all zero values from budget and revenue columns because they would have affected the accuracy of my conclusions from the analysis. There are still a few outliers even after the omissions but even then we can still see that there is a positive correlation beteen both buget and number of votes with revenue.

### References

1.SQL for Business by werty
2. [Stack Overflow](https://stack.com)
