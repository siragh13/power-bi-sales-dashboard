\# Data Cleaning



After reviewing the raw NorthStar Electronics sales data, I cleaned the dataset in Power Query before building the Power BI dashboard.



\## Cleaning Steps



\- Removed duplicate transactions using Order\_ID while keeping one valid copy of each transaction.

\- Checked Order\_ID for missing values.

\- Trimmed text columns to remove unnecessary leading or trailing spaces.

\- Standardized inconsistent capitalization in text columns such as Category, Sales Channel, and other text fields where needed.

\- Kept repeated Product values because the same product can appear in different valid customer transactions.

\- Filtered Quantity to keep values greater than 0.

\- Filtered Unit Price to keep values greater than 0.

\- Filtered Unit Cost to keep values greater than 0.

\- Reviewed the Order Date range. The earliest transaction date was January 1, 2025, and the latest was August 15, 2026.

\- Inspected Product and other text fields for blanks and inconsistent values instead of automatically removing repeated values.



\## What I Learned



One important thing I learned is that a duplicate value in one column does not automatically mean the row is a duplicate transaction. For example, Product names should repeat because different customers can purchase the same product. Order\_ID is the better field for identifying duplicate transactions in this dataset.



I also learned that data cleaning is not just applying transformations. I need to understand what each column represents before deciding whether a value should be changed, removed, or kept.

