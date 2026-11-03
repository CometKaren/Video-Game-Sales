### Step 1: ###
Create a new table for your analysis call “sales_genre”.  Load the table “sales” into this table. Select these columns: Genre, Global_Sales, Critic_Score.  

> CREATE TABLE sales_genre  
> (  
> Genre string,  
> Global_Sales float,  
> Critic_Score int  
> );  
> INSERT OVERWRITE TABLE sales_genre  
> SELECT Genre, Global_Sales, Critic_Score  
> FROM sales;  
> SELECT * FROM sales_genre LIMIT 10;  

### Step 2: ###
Round the data found in the “Global_Sales” column.  (HINT:  the SQL function to round a number is ROUND(obs)

> INSERT OVERWRITE TABLE sales_genre  
> SELECT Genre, ROUND(Global_Sales) AS Global_Sales, Critic_Score  
> FROM sales_genre;  

### Step 3: ###
Filter the data to only look at those items in the “Critic_Score” column that are greater than 0.

> INSERT OVERWRITE TABLE sales_genre  
> SELECT *  
> FROM sales_genre  
> WHERE Critic_Score > 0;

### Step 4: ###
Order the data in the “Critic_Score” column from highest to lowest. (HINT:  Use the DESC query)

> INSERT OVERWRITE TABLE sales_genre  
> SELECT *  
> FROM sales_genre  
> ORDER BY Critic_Score DESC;
