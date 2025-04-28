# Mall Sales Analysis

### Table of contents
- [Project Overview](#project_overview)
- [Recommendations](#recommendations)
### Project Overview

As the business landscape evolves, making strategic decisions through sales data analysis is essential. This analysis explores mall sales data to evaluate product performance, total sales per mall, and overall store performance. The goal is to uncover trends that can drive better decision-making and increase revenue.

### Data Source

Sales Data: The primary dataset used for this analysis is the "Mall_salea_data.csv"file. Conataining detailed information about the sales made by each mall.

### Tools

- Excel -used for data cleaning
- Power BI - used for data visualization
  
### Data Cleaning/Preparation

Being a real word dataset, I performed the following task to be able to use the dataset to obtain insights:
1. Data loading and inspection: Uploaded the file on excel and carefully studied each column to understand what they represent and how they culd help in the analysis.
2. Handling duplicates: Carefully removed duplicates using the invoice number.
3. Handling missing values: Removed column with null values on the quantity column.
4. Creating new columns: Created the sales amount column by multiplying the quantity by unit price.
5. Text Standardization: Changed mAle to Male as standardization aids accuracy of the analysis.

### Research Objective

This project aims to create  visuals and data-driven insights to address the following key questions:
- When is the peak sales period?
- Which product category contribute most to revenue?
- What are the most commonly used payment methods?
- How have sales performed year over year?
- Does the number of customer in each branch affect their total sales?

### Data Analysis
```Power BI
To calculate the sales Year on year(YOY)  the code below was used
Sales_YOY = 
Var PM = CALCULATE([Total sales],DATEADD(Tranx_date[Date],-1,YEAR))
VAR CM = [Total sales]
RETURN
IF(AND(CM,PM),CM/PM-1)

To calculate the average sales the code below

Avg_sales = DIVIDE(SUM('Stores Dataset'[Sales Amount]),COUNT('Stores Dataset'[invoice_no]))
```


### Results

- The mall experience peak sales during the weekend.
- Fashion contributes 60% of the malls total revenue.
- Cash is the most commonly used payment option.
- Sales year on year declined this could be linked to the malls poor customer retention.
- There is a positive correlation between total number of custmers and total sales made by each branch.

### Recommendations

1. Deploy top-performing sales staff to work during the weekends.
2. Ensure there is no stockout period for fashion items.
3. Encourage cashless sales to improve efficiency and save time spent on attending to customers by awarding gift cards to customers when 
   they make purchase up to a particular amount or give discount to customers who use their credit cards to make purchase.
4. Implement upselling and cross-selling strategies via personalized text messages and emails.
5. Launch targeted sales to help boost sales and increase mall customers.

### Limitations

1. The data being a real world data was messy therefore taking much time to clean up.
2. Also the data for 2023 in the data has only records for three months this also affected this analysis because others yeras has records 
   for the complete twelve months hence the three performance for the year 2023 could nt be ascertained.
