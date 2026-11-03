## Data Set and How To Retrieve ##
1.	Go to website: <https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings>
2.	Download data: Video_Game_Sales_as_at_Dec_2016.csv
## Loading Data Set into HDInsight ##
3.	Load your csv file in HDInsight using the Azure Storage Tool.  Put the data in a container called Sales
4.	Create a schema for your data from the raw data.
Using your schema, load the data from Azure Storage into Hive.  Call the table, “sales”.
5.	Validate that the schema is correct using the “table view” tab.
6.	Inspect the data were loaded properly using the SQL query interface
