# Hotel Data Analyst Portfolio Project

## Introduction
Welcome to the Hotel Data Analyst Portfolio Project. In this project, we'll develop a data analytics project using hotel data sourced from a database created by uploading Excel sheets. We will connect this database to Power BI to answer business questions and create a visual product.

## Project Requirements
Our goal is to analyze and visualize hotel booking data. Here are the requirements from our stakeholders:
- Build a visual data story or dashboard using Power BI.
- Answer key business questions:
  - Is our hotel revenue growing by year?
    We have two hotel types, so it would be good to segment revenue by hotel type.
  - Should we increase our parking lot size?
    We want to understand if there is a trend in guests with personal cars.
  - What trends can we see in the data?
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
