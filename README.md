# AdventureWorks
A Power BI Dashboard for Adventure Works, a fictional global manufacturing company that produces cycling equipment and accessories. This Dashboard was done as part of the [Microsoft Power BI Desktop for Business Intelligence Course](https://www.udemy.com/course/microsoft-power-bi-up-running-with-power-bi-desktop/?couponCode=KEEPLEARNING) by Maven Analytics. 

[Please click here to interact with the dashboard yourself](https://app.powerbi.com/view?r=eyJrIjoiYjg1MDI5ZDUtNTk4Yy00MDllLTliYjYtNTM2NWE1ZjE3MzMwIiwidCI6ImM2N2EyZTU0LTE2NGItNDVkYS1iNDdlLTEwZjkzZTU0M2ZmMyJ9)


![image](https://github.com/AliMamdouhSalem/AdventureWorks/assets/74428524/0d02e8ef-6365-48f2-924d-f156243ea7c6)


# Data
The data set can be found on [AdventureWorks sample databases](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms) and in the project it consists of the following CSV files:

- Sales Data for 2020, 2021, and 2022
- Customer Lookup
- Product Categories Lookup
- Product Subcategories Lookup
- Returns Data
- Territory Lookup
- Calendar Lookup

# Transformation
Several Cleaning and transformation steps were done using Power Query Editor like:

- Used the Power Query Editor to expand on the date column in calendar lookup to create several date columns like start of week, start of month, start of quarter, start of year and many more.
- Used text formatting tools to split data from columns into new ones, Capitalize each word and others.
- Created a date key in several table by turning the date column into text and then removing the '/'
- Renamed Columns and removed others that weren't needed
- Appended the three Sales Data CSVs into one table

Those are only examples, please check the report file to see all the transformations, calculated columns, and measures that were done.

# Model 
Used Dimensional modelling techniques to model the data into two facts 

- Sales Data
- Returns Data
  
All the other tables were dimensions for these 2 facts.

![image](https://github.com/AliMamdouhSalem/AdventureWorks/assets/74428524/c7427b03-ac5b-47b6-8d8b-69b5ec128b8b)

# Dashboard 
This Dashboard has 4 different pages.

## Executive Summary
This page has a top level view for AdventureWorks Executives.

![Executive Dashboard](https://github.com/AliMamdouhSalem/AdventureWorks/assets/74428524/5f5f2067-5aa3-4e7c-9fc3-da01ca075cf4)

It contains the following Visualisations:

- KPIs for the Total Revenue, Net Profit, Orders and Return Rate
- A line chart showing the revenue trending by start of month
- A bar chart showing the amount of orders by product category
- Three KPI charts showing the latest month's revenue and comparing it with the targeted value
- A matrix table for top 10 products by revenue with their number of orders, revenue and return
- Cards for the most ordered product type and most returned product type

## Product
This page is a drillthrough page to drill by a certain product and get valuable insights about it. 

![Product Dashboard](https://github.com/AliMamdouhSalem/AdventureWorks/assets/74428524/16d4f93e-816c-4496-acf0-58ef23551010)

It contains the following Visualisations:

- A card for the drilled by product name
- Three gauge charts for monthly order, revenue and profit vs. their targets
- A line chart for profit vs. adjusted profit with a slider that controls the precentage the adjusted profit is going to increase or decrease
- An area line chart that has a slicer that can toggle between revenue, returns, profit and return rate

## Customer 
This page shows customer insights.

![Customers Dashboard](https://github.com/AliMamdouhSalem/AdventureWorks/assets/74428524/229234a1-b93d-4f85-bb08-d7746829dec9)


It contains the following Visualisations:

- Two cards for the total number of customers and the average revenue per customer
- A line chart that can be toggled with a slicer between customer trending and revenue per customer per month
- Two Donut Charts for total number of orders by income level and by occupaton  
- A matrix table for the top 100 customers showing customer id, full name, orders, and revenue per customer
- Three Cards for the top customer by revenue and this customer's total orders and revenue

## Map
This page contains a map of the world with bubbles which are bigger and smaller depending on the number of orders for each country with a slicer that switches between different continents.

![Map](https://github.com/AliMamdouhSalem/AdventureWorks/assets/74428524/b0c8dcb3-6a4a-4d52-b873-3209c522eb3b)


