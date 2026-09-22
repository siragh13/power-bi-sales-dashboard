\# Dashboard Development



\## Project Goal



After cleaning the NorthStar Electronics sales data, I built an interactive Power BI report to analyze overall business performance and identify the products and sales representatives driving revenue and profit.



The report contains two pages:



1\. Executive Overview

2\. Product \& Sales Analysis



\## DAX Measures



I created measures instead of relying only on the raw dataset because some of the business metrics requested for the dashboard were not included in the original data.



\### Total Revenue



Total Revenue calculates sales revenue using quantity sold and unit price.



Total Revenue = SUMX(SalesTransactions, SalesTransactions\[Quantity] \* SalesTransactions\[Unit\_Price])



\### Total Profit



Total Profit calculates the amount remaining after product cost.



Total Profit = SUMX(SalesTransactions, SalesTransactions\[Quantity] \* (SalesTransactions\[Unit\_Price] - SalesTransactions\[Unit\_Cost]))



\### Profit Margin



Profit Margin compares total profit with total revenue.



\### Total Orders



Total Orders counts unique Order IDs rather than simply counting rows.



\### Units Sold



Units Sold calculates the total quantity of products sold.



\## Date Analysis



I created a separate DateTable to support time-based analysis.



The DateTable includes fields such as:



\- Date

\- Month

\- Month Number

\- Quarter

\- Year

\- Year Quarter

\- Year Quarter Sort



Month Number was used to keep month names in chronological order.



I also created measures for previous-quarter revenue and quarter-over-quarter revenue change. The dashboard displays an up arrow for positive revenue change and a down arrow for negative revenue change, with conditional colors to make the direction easier to identify.



\## Executive Overview



The Executive Overview page was designed to answer the question:



\*\*How is the business performing overall?\*\*



The page includes KPI cards for Total Revenue, Total Profit, Profit Margin, Total Orders, and quarter-over-quarter revenue change.



It also includes:



\- Revenue trend by month

\- Revenue and profit by category

\- Revenue by region

\- Revenue by sales channel

\- Year Quarter slicer



\## Product \& Sales Analysis



The Product \& Sales Analysis page was designed to answer:



\*\*What products and sales representatives are driving business performance?\*\*



The page includes:



\- Product-level table showing Units Sold, Total Revenue, and Total Profit

\- Revenue by Product ranking

\- Revenue by Sales Rep treemap

\- Revenue and Profit by Sales Rep comparison

\- Revenue vs Units Sold by Product scatter/bubble chart

\- Year Quarter and Category slicers



For the scatter chart, Units Sold is used on the X-axis and Total Revenue on the Y-axis. Unit Price is represented through bubble size. This helps show why a product with fewer units sold can still generate more revenue when its unit price is higher.



\## Filtering and Interactions



The report uses slicers and visual interactions so users can explore the data without changing the underlying dataset.



The Product \& Sales Analysis page can be filtered simultaneously by Year Quarter and Category.



Missing Sales Rep values were kept in the underlying transaction data because the transactions were still valid for company-level financial analysis. However, blank Sales Rep values were excluded from the sales-representative performance visual using a visual-level filter.



\## Report Design



I used a light dashboard design with consistent spacing, borders, titles, and blue/teal accents across both pages.



Conditional formatting was also used to make important changes and values easier to identify visually.



\## Validation



I tested the report by:



\- Comparing unfiltered dashboard totals with the expected dataset totals

\- Testing Year Quarter and Category slicers together

\- Testing interactions between visuals

\- Confirming that sales-representative blank values were excluded only where appropriate

\- Confirming that measures and visuals updated correctly when filters changed



The final unfiltered totals used for validation were:



\- Units Sold: 8,510

\- Total Revenue: $2,665,563.86

\- Total Profit: $876,467.86

