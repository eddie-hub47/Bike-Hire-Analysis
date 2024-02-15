# Hire Trend Analysis

## Table of Contents

 - [Project Overview](#project-overview)
 - [Data sources](#data-sources)
 - [Tools](#tools)
 - [Data Cleaning](#data-cleaning)
 - [Exploratory Data Analysis](#exploratory-data-analysis)
 - [Data Analysis](#data-analysis)
 - [Results](#results)
 - [Recommendations](#recommendations)
 - [Limitations](#limitations)
 - [Reference](#reference)

### Project Overview

This data analysis offers insights into the three distinct bike types utilized by the company for its rental services. Through the comparison and analysis of each bike type's data, our goal is to discern trends, enhance our understanding of diverse bike usage patterns, and assess the overall performance of the company.


### Data sources 

The main dataset utilized in this analysis is the "bike_project_csv" file, encompassing the performance of each bike type throughout January 2022.


### Tools

- Excel - Data Cleaning
   - [Download Here](https://microsoft.com)
     
- MySQL server - Data Analysis
   - [Download Here](https://sqlserverdownload)
     
- Tableau - Data visualization
   - [Download Here](https://tableau.com)


### Data Cleaning

During the initial stage of data preparation, the following tasks were undertaken:
1. Importing data into Excel
2. Examing data headers
3. Formatting the data
4. Addressing Null values
5. Scanning the data for duplicates and removing empty cells


### Exploratory Data Analysis

EDA was performed to answer some key business questions which include:

- During January 2022, which bike type was the most popular and frequently rented among riders? (Keep in mind that there are two distinct categories of riders: Members and Casual riders.)
- At what times of the day are the bikes predominantly in use by riders?
- Which bike station experienced the highest number of bike rides?

 ### Data Analysis

 ´´´Mysql
 SELECT Member_casual, COUNT (Member_casual) AS Proportion_of_Riders
 FROM Cyclic1
 GROUP BY Member_casual
 
 SELECT TOP 1 Rideable_type, COUNT(Rideable_type) AS Ride_type
 FROM Cyclic1
 WHERE Member_casual = 'Member'
 GROUP BY COUNT(Rideable_type) DESC

 SELECT TOP 1 Start_station_name, COUNT(Ride_id) AS Count 
 FROM Cyclic1
 GROUP BY Start_station_name
 ORDER BY COUNT(Ride_id) DESC
 ´´´


 ### Results

After the analysis, the findings to address the business concern can be summarized as follows:
1. The classic bike type stands out as the favored choice among both member and casual riders. It is advisable to contemplate investment in classic bikes.
2. Member riders exhibit peak activity during the morning at 7 am and in the evening at 5 pm, with the highest peak occurring in the evening, boasting 7148 riders. Casual riders, on the other hand, reach their highest peak at 5 pm, with 1078 riders.
3. Kingsbury St & Kinzie St emerges as the most bustling station, recording a total of 1047 rides.


### Recommendations 

In light of the findings from the analysis, I Propose the following course of actions
1. Consider investing in classic bikes, as they are the preferred choice among most riders. This investment has the potential to enhance rental turnover, thereby boosting overall business performance.
2. If capital constraints prevent the purchase of classic bikes, explore the option of renting them at peak hours, specifically at 7 am and 5 pm, to maximize profitability.
3. Prioritize the expansion of parking slots in Kingsburg St and Kinzie Station to increase the availability of classic bikes for rental purposes.

### Limitations

In conducting this analysis, I needed to eliminate null values and deleted empty cells to ensure the accuracy of my findings.


### Reference

1. Jupita Academy Data Analysis Assignment
2. [Stack Overflow](https://stackoverflow.com)
