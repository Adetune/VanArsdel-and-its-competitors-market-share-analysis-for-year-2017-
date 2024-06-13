# VanArsdel and its competitors
## market share analysis for year 2017
## Excel to Power BI Project





# Table of contents 

- [Objective](#objective)
- [Data Source](#data-source)
- [Stages](#stages)
- [Design](#design)
  - [Mockup](#mockup)
  - [Tools](#tools)
- [Development](#development)
  - [Pseudocode](#pseudocode)
  - [Data Exploration](#data-exploration)
  - [Data Cleaning](#data-cleaning)
  - [Transform the Data](#transform-the-data)
  - [Create the SQL View](#create-the-sql-view)
- [Testing](#testing)
  - [Data Quality Tests](#data-quality-tests)
- [Visualization](#visualization)
  - [Results](#results)
  - [DAX Measures](#dax-measures)
- [Analysis](#analysis)
  - [Findings](#findings)
  - [Validation](#validation)
  - [Discovery](#discovery)
- [Recommendations](#recommendations)
  - [Potential ROI](#potential-roi)
  - [Potential Courses of Actions](#potential-courses-of-actions)
- [Conclusion](#conclusion)




# Objective 

- What is the key pain point?
  
- Chief Marketing Officer (CMO) wants to know how well does VanArsdel product sell within the industry the for year 2017.
- Also, how well is VanArsdel doing against their competing product in the industry for the year 2017.


- What is the ideal solution? 

To create a dashboard that provides insights into the VanArsdel and its competitors market share analysis for year 2017 that includes their 
- Revenue and Unit by Month
- Revenue by Manufacturer
- Sum of Revenue by Segment
- Sum of Revenue by MonthName and Manufacturer(groups)
- Sum of Revenue by State and Segment
- Sales by State

This will help the Chief Marketing Officer (CMO) make informed decisions about how well does VanArsdel product sell and how well is VanArsdel doing against their competing product in the industry for the year 2017.

## User story 

As the the Chief Marketing Officer (CMO) of VanArsdel Company, I want to use a dashboard that analyses how well our company product sell in 2017. 
This dashboard should allow me to identify how well is our product doing against our competing product in the industry for the year 2017.
This dashboard should allow me to analyse sales revenue accross all manufaturers on the year 2017. 
This dashboard should allow me to analyse revenue by manufaturers on the year 2017.
This dashboard should allow me to analyse sales by segment on the year 2017. (Segment report).
This dashboard should allow me to compare VanArsdel sales and revenue with other competitors.
This dashboard should allow me to identify or show the market shares analysis.
This dashboard should allow me to analyse Sales by State
This dashboard should allow me to compare revenue by category and state in tabular view.

With this information, I can make more informed decisions abouthow well our company VanArsdel product sell in 2017.
Also how well VanArsdel product doing against our competing product in the industry for the year 2017. 


# Data source 

- What data is needed to achieve our objective?

We need data on the VanArsdel Company in 2017 that includes their 
- sales
- product
- geograpy
- date

   Where is the data coming from? 
Sales data along with details of Product, Date and Geography are available in an Excel workbook. Data from these sources need to be brought together to analyze and report on.

# Stages (ETL)
- Import Data
- Clean Data
- Manage relationship
- Design
- Developement
- Testing
- Analysis 

##  Import Data
- Get Data

## Transform Data
- Clean Data

## Manage relationship
- We need to load data from 4 tables
- We need to ensure the model identifies relationship between these tables.
  
# Design 

## Dashboard components required 
- What should the dashboard contain based on the requirements provided?

 To understand what it should contain, we need to figure out what questions we need the dashboard to answer:
1. Any sales that happened, we want to analyse it by month for year 2017 for each manufactural 
2. Who is contributiing more total sales?
3. Which seginment is making the highest sales?
4. Which company is making the highset market shares?
5. To compare VanArsdel with the rest of the competitors

For now, these are some of the questions we need to answer, this may change as we progress down our analysis. 


## Dashboard mockup

- What should it look like? 

Some of the data visuals that may be appropriate in answering our questions include:

1. Line and Clustered Column chart
2. Treemap chart
3. Donut chart
4. Stacked area chart
5. Map visual 
6. Matrix visual 



![Dashboard-Mockup](assets/images/dashboard_mockup.png)


## Tools 


| Tool | Purpose |
| --- | --- |
| Excel | Exploring the data |
| Power BI | Cleaning, testing, and analyzing the data |
| Power BI | Visualizing the data via interactive dashboards |
| GitHub | Hosting the project documentation and version control |
| Mokkup AI | Designing the wireframe/mockup of the dashboard | 


# Development

## Pseudocode

- What's the general approach in creating this solution from start to finish?

1. Get the data
2. Explore the data in Excel
3.Transform the data in Power BI
5. Clean the data with Power BI
6. Load the data into Power BI
7. Test the data with Power BI
8. Visualize the data in Power BI
9. Generate the findings based on the insights
10. Write the documentation + commentary
11. Publish the data to GitHub Pages

## Data exploration notes

This is the stage where you have a scan of what's in the data, errors, inconcsistencies, repitetions, weird and corrupted characters etc  


- What are your initial observations with this dataset? What's caught your attention so far?

1. There are at least 4 tables that contain the data from these sourcesthat is  need for to be brought together to analyse and report on, which signals we have everything we need from the file without needing to contact the VanArsdel company and competitors for any more data. 
2. The Date table contains the Month column, this is a repetition we do not need Month column -  we need to remove  Month column from the Date column.
3. The product table contains the Product Name and Product ID is concatenated in Product column, we need to split it so that we have just the Product Name. -  we need to use Split Column by Delimiter, Enter “-“ in the text area. Product column is split into two columns Product.1 and Product.2. We do not need Product.2 since we already have a ProductID column. Remove Product.2 and Rename Product.1 to Product.
4. We have now transformed all the data in the query editor, then we close and apply to load all the tables into Power BI 


- What do we expect the clean data to look like? (What should it contain? What contraints should we apply to it?)

The aim is to refine our dataset to ensure it is structured and ready for analysis. 

The cleaned data should meet the following criteria and constraints:

- Only relevant columns should be retained.
- All data types should be appropriate for the contents of each column.
- No column should contain null values, indicating complete data for all records.


Below is a table outlining the constraints on our cleaned dataset:

| Description | Date |
| --- | --- |
| Number of Rows | 731 |
| Number of Columns | 5 |

| Description | Product |
| --- | --- |
| Number of Rows | 1,245 |
| Number of Columns | 7 |

| Description | Geo |
| --- | --- |
| Number of Rows | 7,416 |
| Number of Columns | 6 |

| Description | Sales |
| --- | --- |
| Number of Rows | 117,917 |
| Number of Columns | 5 |


- What steps are needed to clean and shape the data into the desired format?

1. Remove unnecessary columns by only selecting the ones you need
2. Extract Youtube channel names from the first column
3. Rename columns using aliases
   
   
## Manage relationship

