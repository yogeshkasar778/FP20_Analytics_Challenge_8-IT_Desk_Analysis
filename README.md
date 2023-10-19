# :ticket: FP20 Analytics Challenge 8-IT Help Desk Analysis

![image](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/assets/118357991/4643fa9c-9025-40df-9ffc-af36e8981c31)

## Table of Contents :

- [Problem Statement](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/edit/main/README.md#dart-problem-statement-)
- [Data Gathering / Requirement](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/edit/main/README.md#data-gathering--requirement)
- [Data Perparation](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/edit/main/README.md#data-preparation)
- [Data Modelling](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/edit/main/README.md#data-modelling)
- [Data Analysis Expression (DAX) Calculation ](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/edit/main/README.md#data-analysis-expression-dax-calculation-)
- [Report](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/edit/main/README.md#chart_with_upwards_trend-report)
- [Dashboard](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/edit/main/README.md#bar_chart-dashboard)
- [Tools, Software](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/edit/main/README.md#tools-software-)

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

- `IT Tickets` which has `97499 rows and 10 Column` of observation.
- `IT Agents` which has `50 rows and 8 Column` of observation.

## Data Modelling:
Then dataset was cleaned and transformed, it was ready for data modeled.

- The `IT Tickets and Agents` tables as shown below:

We will create the data model connecting all tables and utilize the Calendar table that has already been set up.

![image](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/assets/118357991/e2f9a5b0-7052-4ce9-84c4-eb79695c9290)

## Data Analysis Expression (DAX) Calculation :
Measures used in visualization are:

  - `Total Agents = COUNT(IT_Agents[Agent ID])`
  - `Total Ticket = COUNT(Tickets1[ID Ticket])`
  - `Avg. Agent Age = AVERAGE(IT_Agents[Age])`
  - `Avg. Resolution Time = AVERAGE(Tickets1[Resolution Time (Days)])`
  - `Avg. Satisfaction Rate = AVERAGE(Tickets1[Satisfaction Rate])`
  - `Issue type IT Error = CALCULATE(COUNT(Tickets1[ID Ticket]),Tickets1[Issue Type]="IT Error")`
  - `Issue type IT Request = CALCULATE(COUNT(Tickets1[ID Ticket]),Tickets1[Issue Type]="IT Request")`
  - `Outside SLA = CALCULATE(COUNT(Tickets1[ID Ticket]),Tickets1[Resolution]="Outside SLA")`
  - `Within SLA = CALCULATE(COUNT(Tickets1[ID Ticket]),Tickets1[Resolution]="Within SLA")`
  - `Resolution Issue type IT Error = CALCULATE(COUNT(Tickets1[Resolution Time (Days)]),Tickets1[Issue Type]="IT Error")`
  - `Resolution Issue type IT Request = CALCULATE(COUNT(Tickets1[Resolution Time (Days)]),Tickets1[Issue Type]="IT Request")`

Date Calculation:

  - `DateMaster = CALENDAR(FIRSTDATE(Tickets1[Date]),LASTDATE(Tickets1[Date]))`
  - `Month = MONTH(DateMaster[Date])`
  - `Year = YEAR(DateMaster[Date])`
  - `Month Name = FORMAT(DateMaster[Date],"MMM")`
  - `Month Order = DateMaster[Date].[MonthNo]`
  - `Quertor = QUARTER(DateMaster[Date])`
  - `Week Day = WEEKDAY(DateMaster[Date])`
  - `Week Day Name = FORMAT(DateMaster[Date],"DDD")`
  - `Year = YEAR(DateMaster[Date])`

## :chart_with_upwards_trend: Report:
Data visualization for the dataset was done using Microsoft Power BI Desktop:

View Report - [Report](https://app.powerbi.com/links/NZvsjlKN3L?ctid=b9cd496c-35ed-4f56-9942-e91f9a3d8d48&pbi_source=linkShare)

|    Tickets      |
| --------------- |
|![image](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/assets/118357991/0fde3909-3319-44c2-b80b-c7205478020c)|

|    Agents      |
| --------------- |
|![image](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/assets/118357991/7cf79a5f-d207-4d02-8146-f56287b7835a)|

## :bar_chart: Dashboard:


|    Dashboard    |
| --------------- |
|![image](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/assets/118357991/6a307403-44d4-48b4-aff9-432531bfb714)
![image](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/assets/118357991/ef55057a-ac31-42a3-a4e6-925a7ef0e111)
![image](https://github.com/yogeshkasar778/FP20_Analytics_Challenge_8-IT_Help_Desk_Analysis/assets/118357991/5e1f4fd5-6754-4b4b-bdd6-347ecbd85b31)|


## Tools, Software :

1. Power BI

2. Power Query Editor

3. Power BI Service

4. Power BI Desktop

5. Power BI Dashboard
   
6. DAX

7. Excel

***
