# :ticket: FP20 Analytics Challenge 8-IT Help Desk Analysis

## Table of Contents :

- [Problem Statement](https://github.com/yogeshkasar778/Denis-Retail_sales_report_and_dashboard#problem-statement-)
- [Data Gathering / Requirement](https://github.com/yogeshkasar778/Denis-Retail_sales_report_and_dashboard#data-gathering--requirement)
- [Data Gathering and Integration](https://github.com/yogeshkasar778/Denis-Retail_sales_report_and_dashboard#data-gathering-and-integration)
- [Data Modelling](https://github.com/yogeshkasar778/Denis-Retail_sales_report_and_dashboard#data-modelling)
- [Data Analysis Expression (DAX) Calculation ](https://github.com/yogeshkasar778/Denis-Retail_sales_report_and_dashboard#data-analysis-expression-dax-calculation-)
- [Report](https://github.com/yogeshkasar778/Denis-Retail_sales_report_and_dashboard#bar_chart-report)
- [Dashboard](https://github.com/yogeshkasar778/Denis-Retail_sales_report_and_dashboard#bar_chart-dashboard)
- [Tools, Software](https://github.com/yogeshkasar778/Denis-Retail_sales_report_and_dashboard#tools-software-)

## :dart: Problem Statement :

We have gathered data from various sources, including sales data, product information, geography, sales representatives, and categories. The task involves data gathering, data modeling, DAX calculations, 
and creating visuals for the dashboard.

In this challenge, you are presented with a reliable dataset that shows the IT ticket data and Agents’ profiles for a fictitious company that you work for. 
You will provide your actionable insight into your organization's trends, usage patterns, systems behaviours, service level agreement etc. 
It will help our IT department to stay up to date with industry developments. We have gathered data from various sources, including IT Agents and Tickets. The task involves data gathering, data modeling, DAX calculations, 
and creating visuals for the dashboard.

#### In the Tickets Table

- The client requires the canvas settings of the PBI report to be H:1080 - W:1920
- The client would like columns Severity and Priority to be split into 2 columns, creating an ID and classification columns. Example Severity Key column = 0 and Severity Type = Unclassified.
- The Average Resolution time is 4.5 days. The Client would like to create a new column where if the Resolution time is above 3.5 days = "Outside SLA" and if it is below "Within SLA". This will allow the client to push for all calls to stay within the limit by targeting these calls and agents.
  
#### In the IT Agents Table

 - Column Full Name to be split into 2 columns Name and Last Name, where last name is missing to be obtained from the email address column.
 - Name and Last name columns must be Capitalize first words and trimmed.
 - Year/Month/Date of birth must be in one Column - data type Date.
 - The client would also like to know the Age of the Agents from the Agents' DOB 
to 31/12/2020.
    
## Data Gathering / Requirement:
The Dataset used for this challenge was presented by [FP20 Challenges](https://fp20analytics.com/challenges) and Diversity and Inclusion dataset:

Dataset: 
 - [IT Tickets and Agents Table](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/blob/main/IT%20Tickets%20Analysis.xlsx)

## Data Preparation:
Completed the Data transformation in Power Query and the dataset was loaded into Microsoft Power BI Desktop for modeling.

IT Tickets and Agents dataset is given table named:

- `IT Tickets ` which has `97499 rows and 10 Column` of observation.
- `IT Tickets ` which has `50 rows and 8 Column` of observation.


## Data Modelling:
Then dataset was cleaned and transformed, it was ready for data modeled.

- The `IT Tickets and Agents` tables as shown below:

We will create the data model connecting all tables and utilize the Calendar table that has already been set up.

## Data Analysis Expression (DAX) Calculation :
Measures used in visualization are:



## :chart_with_upwards_trend: Report:
Data visualization for the dataset was done using Microsoft Power BI Desktop:

View Report -
## :bar_chart: Dashboard:
Using the measures and calculations, we will design a one-page sales dashboard with various visuals, including charts, graphs, and geo maps. The dashboard will represent sales insights and trends, making it easy to comprehend and facilitate data-driven decision-making.

View Dashboard - 



## Tools, Software :

1. Power BI

2. Power Query Editor

3. Power BI Service

4. Power BI Desktop

5. Power Gateway

6. Excel

***
