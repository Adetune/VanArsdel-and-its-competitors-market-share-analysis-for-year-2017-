# VanArsdel and its competitors
## market share analysis for year 2017






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

This will help the Chief Marketing Officer (CMO) make informed decisions about how well does VanArsdel product sell and how well is VanArsdel doing against their competing product in the industry for the year 2017.

## User story 

As the the Chief Marketing Officer (CMO) of VanArsdel Company, I want to use a dashboard that analyses how well our company product sell in 2017. 
This dashboard should allow me to identify how well is our product doing against our competing product in the industry for the year 2017.
This dashboard should allow me to analyse sales revenue accross all manufaturers on the year 2017.
This dashboard should allow me to analyse revenue by manufaturers on the year 2017.
This dashboard should allow me to analyse sales by segment on the year 2017. (Segment report).
This dashboard should allow me to compare VanArsdel sales and revenue with other competitors.
This dashboard should allow me to identify or show the market shares analysis.



This dashboard should allow me to identify the top performing channels based on metrics like subscriber base and average views. 

With this information, I can make more informed decisions about which Youtubers are right to collaborate with, and therefore maximize how effective each marketing campaign is.


# Data source 

- What data is needed to achieve our objective?

We need data on the top UK YouTubers in 2024 that includes their 
- channel names
- total subscribers
- total views
- total videos uploaded



- Where is the data coming from? 
The data is sourced from Kaggle (an Excel extract), [see here to find it.](https://www.kaggle.com/datasets/bhavyadhingra00020/top-100-social-media-influencers-2024-countrywise?resource=download)


# Stages

- Design
- Developement
- Testing
- Analysis 
 


# Design 

## Dashboard components required 
- What should the dashboard contain based on the requirements provided?

To understand what it should contain, we need to figure out what questions we need the dashboard to answer:

1. Who are the top 10 YouTubers with the most subscribers?
2. Which 3 channels have uploaded the most videos?
3. Which 3 channels have the most views?
4. Which 3 channels have the highest average views per video?
5. Which 3 channels have the highest views per subscriber ratio?
6. Which 3 channels have the highest subscriber engagement rate per video uploaded?

For now, these are some of the questions we need to answer, this may change as we progress down our analysis. 


## Dashboard mockup

- What should it look like? 

Some of the data visuals that may be appropriate in answering our questions include:

1. Table
2. Treemap
3. Scorecards
4. Horizontal bar chart 


