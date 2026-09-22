# NorthStar Electronics Data Assessment



## Project Context



NorthStar Electronics provided a raw sales transaction dataset and requested a Power BI dashboard to analyze revenue, profit, sales trends, product performance, location performance, and sales channels.



Before building the dashboard, I reviewed the raw data to identify issues that could affect the accuracy of the analysis.



## Initial Data Quality Findings



### 1. Revenue and Profit Are Not Included



The client requested revenue and profit analysis, but the raw dataset does not contain Revenue or Profit columns. I noticed that both can be calculated using the available Quantity, Unit Price, and Unit Cost fields.



Revenue = Quantity × Unit Price



Profit = Revenue - (Quantity × Unit Cost)



### 2. Duplicate Transactions



I found eight Order IDs that appear more than once in the dataset. I compared the duplicate Order IDs with their original records and confirmed that the transaction details also match.



These duplicate transactions could cause sales to be counted more than once, which could affect revenue, profit, quantity sold, and other calculations.



The duplicate transactions should be removed during data cleaning while keeping one valid copy of each transaction.



### 3. Missing Values



I found missing values in the Quantity, Unit Price, and Sales Rep columns.



Missing Quantity and Unit Price values are important because they prevent accurate revenue and profit calculations for those transactions. Missing Sales Rep values do not prevent the financial calculations, but they could affect analysis by sales representative.



These missing values need to be investigated and handled appropriately during data cleaning rather than treating every missing value the same way.



### 4. Inconsistent Text Formatting



I noticed inconsistent capitalization in some text fields. For example, the same category can appear with different capitalization, such as Accessories and accessories.



These values represent the same business category, so they should be standardized during data cleaning. Consistent text values help keep grouping, filtering, and reporting reliable.



### 5. Leading and Trailing Whitespace



Some text fields may contain leading or trailing spaces that are difficult to notice during manual inspection.



These spaces should be removed during data cleaning so that text values are consistent and do not cause problems with grouping, filtering, or categorization.

