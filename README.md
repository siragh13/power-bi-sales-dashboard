\# NorthStar Sales Performance Dashboard



An interactive Power BI sales analytics project built to transform raw transaction data into business insights about revenue, profit, product performance, sales representatives, regions, and sales channels.



\## Project Overview



NorthStar Electronics needed a way to understand overall sales performance and identify what was driving revenue and profit.



I worked through the project from raw-data assessment and cleaning to DAX calculations, data modeling, dashboard development, validation, and final report design.



The finished report contains two interactive pages:



\- \*\*Executive Overview\*\* — overall business performance

\- \*\*Product \& Sales Analysis\*\* — deeper analysis of products and sales representatives



\## Dashboard Preview



\### Executive Overview



!\[Executive Overview](images/executive-overview.png)



Quarter filtering dynamically updates KPIs, trends, and quarter-over-quarter revenue change.



\### Product \& Sales Analysis



!\[Product and Sales Analysis](images/product-sales-analysis.png)



Product and sales analysis compares revenue, profit, units sold, and sales representative performance.



\## Dashboard Features



\### Executive Overview



The executive page includes:



\- Total Revenue

\- Total Profit

\- Profit Margin

\- Total Orders

\- Quarter-over-quarter revenue change

\- Monthly revenue trend

\- Revenue and profit by category

\- Revenue by region

\- Revenue by sales channel

\- Year Quarter filtering



\### Product \& Sales Analysis



The analysis page includes:



\- Product revenue ranking

\- Product-level Units Sold, Revenue, and Profit

\- Revenue by Sales Rep

\- Revenue and Profit comparison by Sales Rep

\- Revenue vs Units Sold product analysis

\- Unit Price represented through bubble size

\- Year Quarter and Category filtering



\## Data Preparation



Before building the report, I reviewed and cleaned the transaction data in Power Query.



The process included:



\- Identifying and removing duplicate transactions

\- Handling missing values based on their business impact

\- Standardizing inconsistent text formatting

\- Removing unnecessary whitespace

\- Validating numeric fields used in financial calculations

\- Preserving valid transactions with missing Sales Rep values



\## Data Modeling \& DAX



I created a dedicated DateTable for time-based analysis and developed DAX measures for:



\- Total Revenue

\- Total Profit

\- Profit Margin

\- Total Orders

\- Units Sold

\- Previous Quarter Revenue

\- Quarter Revenue Change



Conditional formatting was used to visually distinguish positive and negative quarter-over-quarter revenue changes.



\## Key Insights



\- Computers were the strongest revenue-generating category, contributing substantially more revenue than the other product categories.

\- Desktop Workstation generated the highest product revenue at approximately $562K and the highest product profit at approximately $166K.

\- Higher unit sales did not always result in higher revenue. Higher-priced products such as Desktop Workstation generated more revenue despite selling fewer units than several lower-priced products.

\- Revenue was distributed fairly evenly between Online and Business sales channels, while Retail contributed a slightly smaller share.

\- Overall sales generated approximately $2.67M in revenue and $876K in profit, with a profit margin of about 33%.



\## Design Decisions



\- I used separate Executive Overview and Product \& Sales Analysis pages to keep high-level business performance separate from detailed analysis.

\- I used a scatter chart to compare units sold with revenue because high sales volume does not always mean high revenue.

\- I used conditional formatting for quarter-over-quarter revenue change so increases and decreases can be identified quickly.



\## Tools \& Skills



\- Power BI Desktop

\- Power Query

\- DAX

\- Data Cleaning

\- Data Modeling

\- Data Visualization

\- Dashboard Design

\- Business Analysis

\- Git \& GitHub



\## Project Documentation



Additional documentation is available in the `docs` folder:



\- `data-assessment.md` — initial review of the raw dataset

\- `data-cleaning.md` — data-cleaning decisions and process

\- `dashboard-development.md` — DAX, report development, design decisions, interactions, and validation



\## Validation



The completed report was tested using slicers, visual interactions, and known totals.



Final unfiltered results:



\- \*\*Units Sold:\*\* 8,510

\- \*\*Total Revenue:\*\* $2,665,563.86

\- \*\*Total Profit:\*\* $876,467.86



\## Repository Structure



```text

power-bi-sales-dashboard/

├── data/

├── docs/

│   ├── data-assessment.md

│   ├── data-cleaning.md

│   └── dashboard-development.md

├── NorthStar\_Sales\_Dashboard.pbix

└── README.md

