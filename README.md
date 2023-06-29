# Hive-Zippelin-HDFS-Exploring Worldwide Sales

## Introduction:
The goal of this project was to use Zeppelin and HDFS to analyze a global sales dataset. Zeppelin was used to import the data, while Spark's basic Scala commands and SQL were used for querying. The analysis was focused on providing a thorough breakdown of the sales data and identifying significant insights into sales patterns and trends.
Zeppelin and HDFS were used to import the data into a dataframe as the initial stage of the investigation. A visual inspection of the data was then possible thanks to the data being presented in the data frame format. The dataframe's schema, which offers a systematic overview of the variables and data types in the dataset, was printed as the next step.

## Tools Used:
- Zeppelin
- Spark
- HDFS
- SQL
- Scala

## Process:
1. Load data into a Spark dataframe.
![image](https://user-images.githubusercontent.com/132706047/249648933-eecba10e-11b7-4ca7-9687-afb5fc187f42.png)

2. Print the dataframe schema.
![image](https://user-images.githubusercontent.com/132706047/249655649-21666ed2-abf7-4885-983a-32f9b7cfc673.png)

3. Filter the dataframe to show units sold greater than 8000 and unit cost greater than 500 ("&&" operator can be used for multiple "AND" conditions).
![image](https://user-images.githubusercontent.com/132706047/249655679-1a756b47-34f0-4ca2-8bf0-19175106b04a.png)

4. Aggregate the dataframe via group by “Region” and count.
![image](https://user-images.githubusercontent.com/132706047/249655692-a80cba50-781f-4e62-a8b1-b0827a7ff8cd.png)

5. Create a separate dataframe with the above group by results.
![image](https://user-images.githubusercontent.com/132706047/249655702-f07f7b38-63de-4704-857d-c57828c5c4a0.png)

6. Save this new subset dataframe as a csv file into HDFS – make sure it is saved as a single file in HDFS.
![image](https://user-images.githubusercontent.com/132706047/249655712-01a591b6-c15e-410f-83d5-03861caad113.png)
![image](https://user-images.githubusercontent.com/132706047/249655729-ca8f113a-4544-4478-a3c6-26935e4a5413.png)

7. Create two views using the “createOrReplaceTempView” command.
![image](https://user-images.githubusercontent.com/132706047/249655748-256a9216-3da4-49c1-9ef8-48932fab7dbc.png)

8. View on “Salesview” from the first dataframe.
![image](https://user-images.githubusercontent.com/132706047/249655771-585c9227-3a5d-456d-930e-ddb378a83007.png)
![image](https://user-images.githubusercontent.com/132706047/249655786-c27826a7-05a5-4489-b495-a407b3ac0b9b.png)

9. View on “Regionview” from the second dataframe.
![image](https://user-images.githubusercontent.com/132706047/249655812-8a6b63a6-bcab-472a-ad67-7ff5a2d8a631.png)
![image](https://user-images.githubusercontent.com/132706047/249655828-ba89712e-0332-4afe-bac3-e3109428f60e.png)

10. Using SQL select all from “Regionview” view and show in a line graph.
![image](https://user-images.githubusercontent.com/132706047/249655850-651d1879-4192-4a30-9ac7-5cd6025b87b6.png)

11. Using SQL, from the “Salesview” view, Select the region and sum of units sold, and group by region.
![image](https://user-images.githubusercontent.com/132706047/249655868-fd8d06cd-e2a5-456e-a0ab-fd0c89cab591.png)

12. Using SQL select from the “Salesview” view – the region and sum of total_profit and group by region and display in a Bar chart.
![image](https://user-images.githubusercontent.com/132706047/249655880-8c329caf-c29c-46cc-8411-4e8c7982d496.png)

13. Using SQL select from the “Salesview” view – show the total profit as profit, the total revenue as revenue and the total cost as cost from “Salesview”, group by region.
![image](https://user-images.githubusercontent.com/132706047/249655895-c0e6dc98-50b6-4c46-808b-56b662a8e5ae.png)

14. The client is in the process of opening up a new store and they are looking at the best location to do so - They need to see the avg profit in each region as a percentage (pie chart) compared to other regions.
![image](https://user-images.githubusercontent.com/132706047/249655906-51b1eee0-3ab6-4457-9d27-d923bec5247f.png)
