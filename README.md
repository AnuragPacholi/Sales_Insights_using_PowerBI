# Sales_Insights_using_PowerBI

Using PowerBi we have taken sales insights from the chosen database.<br>
You can see the final preview in the images given above in the repo.<br>
You can also download the video given above in the repo to see how the sales insights works.<br>
This sales insights project will work on both PC and Mobile, thanks to all the amazing features provided in PowerBI.

## Setup mysql on your computer:
1. Follow this video to install mysql on your computer -<br>
[Install MYSQL](https://www.youtube.com/watch?v=WuBcTJnIuzo)
2. SQL database is in the database.sql file above. Download file to your computer and import it as per instructions given in the tutorial video.

## Setup PowerBI on your computer:
1. Open Microsoft Store.
2. Search for PowerBI
3. Click on "**Get**" to Download and Install.
4. Add the database.

## Data Manipulation in PowerBI:
We need to transform the database a little bit before we can take insights from it. Use the following code in powerbi to transform the database:
```
= Table.AddColumn(#"Filtered Rows", "norm_amount", each if [currency] = "USD" or [currency] ="USD#(cr)" then [sales_amount]*75 else [sales_amount], type any)
```
