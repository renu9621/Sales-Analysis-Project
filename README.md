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

![Avg order value](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/c271cd68-611e-4a1c-b055-2a2e7c152e24)

Step 2 : New measure was created to find total number of orders.

Following DAX expression was written for the same,
        
        Total Orders = DISTINCT COUNT(pizza_sold[order_id])
        
A card visual was used to represent total revenue.

![Avg order value](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/c271cd68-611e-4a1c-b055-2a2e7c152e24)

Step 3 : New measure was created to find average order value.

Following DAX expression was written for the same,
        
        Avg Order Value = [Total Revenue]/[Total Orders]
        
A card visual was used to represent total revenue.

![Avg order value](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/c271cd68-611e-4a1c-b055-2a2e7c152e24)

Step 4 : New measure was created to find average pizzas per order.

Following DAX expression was written for the same,
        
        Avg Pizzas Per Order = [Total Pizza Sold]/[Total Orders]
        
A card visual was used to represent total revenue.

![Avg order value](https://github.com/renu9621/Sales-Analysis-Project/assets/155563588/c271cd68-611e-4a1c-b055-2a2e7c152e24)

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
