we will follow the some steps to build the best portfolio as a data analyst:

Create a Database
Query and analyze data with SQL
Integrate Power BI with a Database
Create Data Visualizations Using Power BI
1. Create a Database
Let’s start by creating a database in SSMS (SQL Server Management Studio) for further analysis of Hotel Booking Data. Find all the data you need here.

We will create a database by following these steps:

Open SQL Server Management Studio and you will see a new window on your screen.

IMAGE 1

Copy the Server Name for later use, then click on Connect.
Now on SSMS window you will see the following options.

IMAGE 2

Right click on Databases and select New Database from the drop down.

IMAGE 3

Assign a Database Name in New Database window and click OK.

IMAGE 4

Expand the Databases and you can see Project database is created.

IMAGE 5

In the Databases pane, right-click the Project database and select Import Data from Task drop down list.

IMAGE 6

In the Import Data dialog box, select the data source that you want to import from.
Browse data file or enter path.
Choose the excel version you want to use and click Next.

IMAGE 7

Note: If you are facing the following error on clicking Next just download Microsoft Access Database Engine 2016.

iMAGE 8

Select a destination and verify the server and database name.

IMAGE 9

Select tables that you want to import.

IMAGE 10

Now, when you run it immediately, you will see that all the data is imported into the environment.

IMAGE 11

You can then view the data in the Project database by expanding the Tables node in the Databases pane.

IMAGE 12

2. Querying data
We have now prepared our data tables in the database for SQL commands. Let’s now apply some commands to explore the data.

Fetching Data from Tables
To fetch data to view from the tables, we will use the following command. The wildcard ‘*’ operator is used to retrieve all the data from the table.

IMAGE 13

After executing the commands, the data will be displayed like this:

IMAGE 14

Combining the Data
To combine the data from the three tables, we simply use the UNION operator among these commands.

IMAGE 15

IMAGE 16

3. Exploratory Data Analysis (EDA)
Now, we are going to apply EDA on the data and try answer the following questions.

Is our hotel revenue growing yearly?
Should we increase our parking lot size?
What trends can we see in the data?
Before answering the questions, we will first create a single temporary table hotels that combines all the data using following code for easier access and analysis.

IMAGE 17

Q.1: Is our hotel revenue growing yearly?
In our dataset we don’t have revenue, but we do have adr (Average Daily Rate), stays_in_week_nights, and stays_in _weekend_nights. So, we will create a new column revenue by using the data of these three columns as follows.

IMAGE 18

The revenue column is here.

Let’s bring another column arrival_date_year from the data and then calculate the sum of revenue while grouping the data by year.

IMAGE 19

Now, in the following table, we can see that the revenue increased from 2018 to 2019 but then decreased again in 2020.

IMAGE 20

We can also determine the revenue trend by hotel type by grouping the data by hotel and then seeing which hotels have generated the most revenue.

IMAGE 21
IMAGE 22

Q.2: Should we increase our parking lot size?
To answer this question, we will focus on the car_parking_spaces and number of guests staying in the hotel. So, let’s do it by applying the following SQL query.

IMAGE 23

In the next table we can observe that we have enough space for parking. So, there is no need to increase our parking lot size.

IMAGE 24

4. Create Data Visualizations Using Power BI
Before moving to Power BI, we need to preprocess some columns.

Using SQL, we will perform two left join queries on the data.

First Left Join: Combines the hotels table with the market_segment table by matching the market_segment column in the “hotels” table with the market_segment.market_segment column.

Second Left Join: Combines the hotels table with the meal_cost table by matching the meal column in the hotels table and the meal_cost.meal column.

IMAGE 25

Now open Power Bi on your PC to connect data base.

Click on Get Data then select SQL Server.

IMAGE 26

A new window titled SQL Server Database will appear.
Enter your server’s name and database name in the respective fields.
Expand the Advanced options and paste the following code in the “SQL text” field.
And click Ok.

IMAGE 27
IMAGE 28

Now you can see that we have brought in our SQL information that we need.
Hit Load button to load the data.

IMAGE 29

Q.3: What trends can we see in the data?
We have created some visuals using Power BI that show some possible trends. Here are a few of them:

Revenue increased from 2018 to 2019, but it began to decrease from 2019 to 2020.
The average daily rate (ADR) has increased from 2019 to 2020, from $99.53 to $104.47.
Total number of nights booked by customers decreased from 2019 to 2020.
The discount percentage offered by the hotel has increased from 2019 to 2020 to attract more customers.

IMAGE 30

Conclusion
In this tutorial, we have covered following topics:

How we can create a database
Manage a database.
Write SQL queries,
How to perform EDA to analyze data
Connect to Power BI for visualization.
 We also tried to answer some questions related to the data.



















# Hotel Data Analyst Portfolio Project

## Introduction
Welcome to the Hotel Data Analyst Portfolio Project. In this project, we'll develop a data analytics project using hotel data sourced from a database created by uploading Excel sheets. We will connect this database to Power BI to answer business questions and create a visual product.

## Project Requirements
Our goal is to analyze and visualize hotel booking data. Here are the requirements from our stakeholders:
- Build a visual data story or dashboard using Power BI.
- Answer key business questions:
  - Is our hotel revenue growing by year? :
    We have two hotel types, so it would be good to segment revenue by hotel type.
  - Should we increase our parking lot size? :
    We want to understand if there is a trend in guests with personal cars.
  - What trends can we see in the data? :
    We must focus on the average daily rate and guests to explore seasonality.

## Project Pipeline
Here’s the project pipeline:
1. Build a database.
2. Develop SQL queries.
3. Connect Power BI to the database.
4. Visualize and summarize findings.

## Data Overview
We have an Excel workbook with several years of hotel data from 2018 to 2019. The workbook includes meal cost, small table, and market segments data.

## Setting Up SQL Server Management Studio
1. Download and install Microsoft SQL Server Studio.
2. Open SQL Server Studio and connect to your server.
3. Note down your server name and default settings for future use.

## Creating a New Database
1. In SQL Server Studio, right-click on `Databases` and select `New Database`.
2. Name the database `project` and click OK.

## Importing Data
1. Right-click on the newly created `project` database, navigate to `Tasks` and select `Import Data`.
2. Choose `Microsoft Excel` as the data source and browse to your data file (e.g., `historical bookings`).
3. Ensure `Microsoft Excel 2016` is selected to avoid issues.
4. Select the destination as `SQL Server Native Client 11.0` and the `project` database.
5. Select the tables to import and click `Next` and `Finish`.

## Verifying Data Import
1. Check the progress of the data import operation.
2. Once complete, verify the tables and their data in the `project` database.

## Writing SQL Queries
1. Navigate to `New Query` in SQL Server Studio.
2. Start exploring your data with SQL commands.
   - Example: `SELECT * FROM dbo.[table_name];`
3. Analyze the data to answer business questions.

## Conclusion
This project will help you develop skills in database creation, SQL querying, and data visualization using Power BI. Completing this project will be a valuable addition to your data analyst portfolio.
