# Maven Toys - Sales Analysis in Power BI
![Maven Toy store image jpg 2](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/925e7593-4a94-4521-94ac-2d40658f185c)

## Background

I recently completed a 3-month data analytics training program at Scenario Academy, where I acquired new data analytics skills. To apply these skills, I worked on a Capstone project focused on sales analysis using Power BI. I analyzed patterns and trends in a dataset from Maven Toy Store, a prominent retailer known for its diverse range of quality products. As a business data analyst, my role was to answer key business questions to support stakeholders in making data-driven decisions. This document outlines my data analysis procedures and insights.

## Business Objectives

The primary goal of the stakeholders is to drive business growth using insights derived from their business data. Therefore, a comprehensive analysis is essential to address these business questions:
1. The top-performing products and their categories.
2. Comparison between the highest selling product and the highest profit margin product.
3. The sales trend and patterns throughout the year.
4. The overall profit the Toy store generates.
5. How much revenue is lost due to products being out-of-stock.
6. How much the business has grown from the previous to the current year.
7. How much financial resources are tied down based on current inventory.

## About the Data

The Maven Toy Store dataset has four CSV sheets (Store, Product, Sales, and Inventory). Each table contains records of 2017 and 2018 historical data.
* Store Table: Contains data on 50 stores and the 29 cities where they are located, including the dates the stores were opened.
* Sales Table: Records over 80,000 units sold on specific dates, providing details about daily transactions.
* Inventory Table: Contains a record of the current level of stock as of the last business date.
* Product Table: Details the 35 products sold at Maven stores, including product price, cost, category, and ID numbers.

#### Analysis Process

The following steps were undertaken to streamline the analysis:
1. Data cleaning and transformation in Power Query.
2. Data modeling.
3. DAX formulas.
4. Data visualization.
5. Interpretation and documentation.

#### Data Importation
I opened the CSV files in Power Query Editor on Power BI workspace to select all the tables and transformed the data for further exploration and cleaning processes.
Data Cleaning
I thoroughly examined each file to check for errors and inconsistencies. The following were carried out in Power Query:
1. Checked the headers for incorrect spellings.
2. Changed the wrong data types to their correct formats.
3. Filtered each column to check for null values, especially in the key columns (Names, ID columns), and found none.
4. Trimmed the tables to remove extra spaces.
I created a calendar table with the CalendarAuto() function to create a date column that starts from the first sales transaction to the last date. I also extracted month and year from the date to form new columns.

![Data Importation](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/6680a98e-955b-4544-8480-4e3c85a4145b)

Data Importation

## Data Cleaning

I thoroughly examined each file to check for errors and inconsistencies. The following were carried out in Power Query:
1. Checked the headers for incorrect spellings.
2. Changed the wrong data types to their correct formats.
3. Filtered each column to check for null values, especially in the key columns (Names, ID columns), and found none.
4. Trimmed the tables to remove extra spaces.
I created a calendar table with the CalendarAuto() function to create a date column that starts from the first sales transaction to the last date. I also extracted month and year from the date to form new columns.

## Data Modeling
Creating relationships between tables is key to accessing data for in-depth analysis. I manually created the relationships between these tables to ensure proper connections. The sales table serves as the fact table, while the store and product tables are connected to sales as dimension tables. The inventory table was connected to both product and store tables.

![Data Modelling](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/ac69ef18-2c0b-4306-a0dc-6c4f1808ae07)

Data Modeling

## Data Analysis

##### Product Category by Profit
According to this analysis, the Toys and Electronics categories were the most profitable product categories from January 1, 2017, to September 30, 2018, with $1,076,527 and $1,001,437 in profits respectively. These account for more than 50% of Maven Toys’ total profit.
In the Toys category, Action Figure and Lego Bricks are the top two products with profits of $347,748 and $298,685 respectively. They also lead in units sold, with Lego Bricks at 59,737 and Action Figure at 57,958.
Colourbuds account for 83.3% of the total profit generated in the Electronics category with $834,944 in profit. The other two products, Gamer Headphones and Toy Robot Electronics, generate a meager amount of profit covering the remaining 16.7%.

![Profit generated by product category](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/b8c8abf0-779f-4385-955e-d9a2e85f1180)

Product Category

#### Inventory Store
The top three stores are situated in two distinct areas: the Airport and Downtown. Two stores, Maven Toys Ciudad de Mexico 2 and Maven Toys Guadalajara 3, are located at the Airport, while the third, Maven Toys Ciudad de Mexico 1, is in Downtown. Across these locations, the Toys and Electronics categories dominate, commanding the largest share of total profits and emerging as the most lucrative categories. Specifically, Electronics yield the highest profits at Airport ($108,197) and Commercial ($287,574) stores, whereas Toys reign supreme at Downtown ($630,029) and Residential ($136,214) outlets.

#### Highest Selling Product

The product with the highest sales is Colourbuds from the Electronics category, followed by PlayDoh Can from the Arts and Craft category, with 104,368 and 103,128 units sold respectively. Colourbuds stand out as not only the product with the highest sales but also the overall best seller at Maven Toys. It grossed $834,944, representing 20.8% of the total profit generated by all 35 products.

![Top 10 Products by units sold](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/9d850859-0b9c-4bed-9842-e622d4632520)

Top 10 products by units sold

Highest Profit Margin Product vs. Highest Selling
Jenga tops the list of highest profit margin products at Maven Toys with a 70% margin, but its overall profit contribution ($91,378) is insignificant. The total sales volume for Jenga (13,054) is much lower compared to Colourbuds (104,368), despite its high profit margin. This low demand might be due to its high markup price. Jenga's sales volume decreased from 2017 (8,009) to 2018 (5,045), while Colourbuds sold 29,156 units in 2018 alone. Colourbuds have a 53% profit margin, which, considering the sales volume, results in $834,944 in profit, accounting for 20.8% of the total profit generated at Maven Toy Store.

![Highest Profit margin vs Highest Selling Product](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/359c989b-47da-41ab-a742-b360426717e0)

Highest Profit margin vs Highest Selling Product

![Highest Profit margin and Highest Selling Product](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/482f37ee-e0a6-4d63-a941-d430d785dcbb)

#### Trends and Patterns

The monthly sales data reflect similar seasonal patterns in 2017 and 2018, with a gradual increase in January, peaking in March and April, then a downward slope until August. The decrease in sales coincides with the summer season when there are more outdoor activities. Sales began to rise again after August in both years. The year-to-date sales data for 2018 stops at September, but it is evident in 2017 that sales continued to rise until December, the highest sales month, coinciding with the festive period.
In 2018, there is a decrease in monthly sales for two months to $722,632 in February, followed by a significant increase in March to $883,515. For the next six months of 2018, the sales data follow a similar trend to that of 2017, remaining relatively constant from April to June and then decreasing from July to September.

#### Overall Profit and Revenue - Comparisons for the Same Period

Despite showing similar trends across different periods of the year, the profit and revenue comparisons within the same period for both years show a significant difference. The units sold, profit, and revenue report a significant difference between these years.

![Monthly revenue trend](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/78b642d8-1922-4d48-92da-db8bbd9f2c25)

Monthly revenue trend

Cumulative sales for September 2018 ($6,962,074) are higher than for September 2017 ($5,320,116). Considering the entire 2017 sales ($7,482,498), 2018 sales from October to December are projected to surpass those of 2017. The number of units sold also follows the same pattern. The total units sold from January to September in 2018 has already surpassed the total units sold for the entire year in 2017. The year-on-year growth percentage (30.9%) between the two years measures the significant increase in sales, vividly illustrating the overall year-on-year growth.

#### Year-on-Year Growth

One of the top product categories, Electronics, suffers a -27% growth due to its 17.9% contribution to sales at the end of September 2018. The Toy category maintains a growth rate of 25.7% over the years, while the Arts and Crafts category tops the chart with a 26.3% growth increase. Maven Toys has been able to maintain profit due to the Arts and Crafts category. Monthly revenue grew from $35,097 in 2017 to $187,230 at the end of September 2018.

#### Revenue Loss

![Revenue loss due to out-of-stock](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/5b007c1d-864f-4306-beec-e5e1897c32b2)

Revenue loss out-of-stock

The inventory analysis reveals that stores with the highest revenues are experiencing shortages of key products, impacting sales. For example, at Maven Toys Ciudad de Mexico 2, Lego Bricks have insufficient inventory to meet daily demand, despite averaging 16.43 units in sales per day with only two units in stock. Similarly, the two leading revenue-generating stores at the Airport, which sell Lego Bricks and ColourBuds, struggle to meet daily demand. In Maven Toys Guadalajara 3, both Lego Bricks and ColourBuds have inadequate stock levels to accommodate their respective average daily sales of 14.63 and 21.43 units, with less than a day's worth of inventory available. Consequently, many of the top 10 revenue-generating products are experiencing shortages in these key stores, resulting in revenue loss for Maven Toys. Failure to meet average daily demand directly correlates with revenue losses.

#### Cost Tied to Inventory
![Revenue tied to invetory](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/67da5445-16f1-47f1-b1fe-0a432fbb13fc)

Revenue tied to inventory

The analysis reveals insufficient stock levels to meet average daily sales. A total of 51,932 units are needed to fulfill daily demand, yet there are only 29,742 units currently available across all stores. Despite this, these stocks are projected to generate $410,240 in sales. By augmenting existing stock levels at the stores, it would be possible to achieve the target average daily sales.

## Data Visualization 

This is the 3-page report for the analysis. The interactive dashboard can be found here.

![Home navigation](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/ca56775f-02a7-4834-b2cf-d29a4edf21e2)

Home navigation

![Product report](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/c593e0eb-601e-4272-a3aa-c2e89e6480f8)

Poduct report

![Store report](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/1e4abfb0-87bf-4a70-8f7e-d0b71ec06675)

Store report

![Trend report](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/3e152c27-e0af-41e4-9333-0a7bc43ea23b)

Trend report

## Recommendation
Maven Toy Store should seek ways to reduce the cost of producing the top products (ColourBuds, Lego Bricks, and Action Figure) to increase their profit margins. This would help save more which is good for business. 
An increase in the inventory stock of top selling products in their respective high demand store locations.
Attention should be paid to Arts and Craft product category; While Electronics sales volume reduced in 2018, Arts and Crafts demand spiked which had the most contribution to the profit for that year by 26%.














