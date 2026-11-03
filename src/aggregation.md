### Step 1: ###
Create two tables showing average critic score for Sports games and average critic score for Shooter games. 

SPORTS GAMES:  
> SELECT AVG(Critic_Score) AS sports_critic_score  
> FROM sales_genre  
> WHERE Genre LIKE “%Sports%”;

SHOOTER GAMES:  
> SELECT AVG(Critic_Score) AS shooter_critic_score  
> FROM sales_genre  
> WHERE Genre LIKE “%Shooter%”;

### Step 2: ###
Create three statistics tables for all games, sports games, and shooter games containing the average, minimum, and maximum global sales.

ALL GAMES:  
> SELECT AVG(Global_Sales) AS average_global_sales, MIN(Global_Sales) AS min_global_sales, MAX(Global_Sales) AS max_global_sales  
> FROM sales_genre;

SPORTS GAMES:  
> SELECT AVG(Global_Sales) AS average_global_sales, MIN(Global_Sales) AS min_global_sales, MAX(Global_Sales) AS max_global_sales  
> FROM sales_genre  
> WHERE Genre LIKE “%Sports%”;

SHOOTER GAMES:  
> SELECT AVG(Global_Sales) AS average_global_sales, MIN(Global_Sales) AS min_global_sales, MAX(Global_Sales) AS max_global_sales  
> FROM sales_genre  
> WHERE Genre LIKE “%Shooter%”;

### Step 3: ###
Create two tables for sports games and shooter games containing the number of games grouped by global sales.

SPORTS GAMES:  
> SELECT Global_Sales, COUNT(Global_Sales) AS count  
> FROM sales_genre  
> WHERE Genre LIKE “%Sports%”  
> GROUP BY Global_Sales;

SHOOTER GAMES:  
> SELECT Global_Sales, COUNT(Global_Sales) AS count  
> FROM sales_genre  
> WHERE Genre LIKE “%Shooter%”  
> GROUP BY Global_Sales;
