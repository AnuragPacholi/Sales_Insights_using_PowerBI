# Sales_Insights_using_PowerBI

## Setup mysql on your computer:
1. Follow this video to install mysql on your computer -<br>
[Install MYSQL](https://www.youtube.com/watch?v=WuBcTJnIuzo)
2. SQL database is in the database.sql file above. Download file to your computer and import it as per instructions given in the tutorial video.

## Data Manipulation in PowerBI:
We need to transform the database a little bit before we can take insights from it. Use the following code in powerbi to transform the database:
```
= Table.AddColumn(#"Filtered Rows", "norm_amount", each if [currency] = "USD" or [currency] ="USD#(cr)" then [sales_amount]*75 else [sales_amount], type any)
```
