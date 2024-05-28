# Sales-Analysis-in-Power-BI
![Maven Toy store image](https://github.com/EniolaIbisanmi/Sales-Analysis-in-Power-BI/assets/130236779/40e421b6-3267-4dde-b293-1ac49112219d)


## Background

I recently completed a 3-month data analytics training with Scenario Academy, where I learned new data analytics skills. To put these new skills into practice, I was assigned a Capstone project on sales analysis using Power BI. I analyzed patterns and trends in a Maven Toy Store dataset to help make informed decisions. Maven Toy Store is a key player in the retail sector, offering a diverse range of quality products. My role was to act as a business data analyst, finding answers to business questions to enable stakeholders to make data-driven decisions. This document shares my data analysis procedures and insights.

## Business Objectives

The stakeholders' major objective is to drive business growth with insights derived from their business data. Hence, a comprehensive analysis is necessary to answer these business questions:
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























