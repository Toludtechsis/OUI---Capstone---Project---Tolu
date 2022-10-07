# OUI-Capstone-Project-Tolu
A capstone project for the OUI Bootcamp : Data Analysis Track.

## Project Background
For the #OUIBOOTCAMP Capstone Project, I was provided with a dataset for the Palmoria Group by REPOTECH as a requirement for completeing the Bootcamp.
The goal of the project is to analyze the HR database of the manufacturing company for gender related issues across the company regions in Nigeria. This documentation will contain:

- Project Objective
- Data Cleaning and Transformation
- Data Modeling
- Data Visualization and Analysis
- Insights
- Recommendations and Conclusions
## Project Objective
In all three of its locations, the Nigerian manufacturing company The Palmoria Group is dealing with problems related to gender imbalance. The headline "Palmoria, the Manufacturing Patriarchy" appeared in the headlines recently, which is regrettable. Given their desire to expand their company to other countries, this doesn't bode well for the business owners. Cases like this can only worsen, exposing additional problems like the gender pay gap among other potential problems. In other to get ahead of any suprises the HR Analyst was charged with identifying potential issues in the gender distribution across the company that can lead to damaging consequences.
### Objectives
-  What is the gender distribution in the organization? Distil to 
  regions and departments
- Show insights on ratings based on gender
  Analyse the company’s salary structure. 
  - Identify if there is a gender pay gap. If there is, identify the 
  department and regions that should be the focus of management
- A recent regulation was adopted which requires 
manufacturing companies to pay employees a minimum of 
$90,000
  - Does Palmoria meet this requirement?
- Show pay distribution of employees grouped by a band of 
   $10,000. For example: How many employees fall into a band of 
   $10,000 – $20,000, $20,000 – $30,000 etc. Also visualize this 
   by regions
- Calculate the amount to be paid as bonus to individual 
   employees
- Calculate the total amount to be paid to individual employees 
  (salary inclusive of bonus)
- Total amount to be paid out per region and company-wide

## Data Cleaning and Transformation
First step was to acquire the dataset from the HR team then to begin the data cleaning process I imported the dataset into PowerBI which is the choiced tool for this analysis. The process of importing the dataset is called GetData to get on with data cleaning I used PowerQuery as a transformation tool to clean the data.
In PowerQuery I took the following steps
- I made sure each column has the right data type and changed the data types where data types didn't match for eachh column
- Promoted first rows as headers
- Filtered for blanks and removed null values 
- I checked for the validity of my data using the column distribution, quality, and profiling from the view tab. 
- Removed leading spaces to ensure there were no uneccessary white spaces
- Removed duplicate values
-  I added an index column to the tables where needed. To give the table a unique identifier column also a called primary key
- Replaced values where genders were not stated with a generic name "Unspecified"
- Removed values not useful for analysis based on an insider hint this include, employees without salary because they are no longer staff, 
  and department that indicated null.
- Executed unpivot to restructure a table within the dataset
- Renamed certain columns so that naming conventions are uniform across board.
- Due to the nature of the dataset provided in order to be able to perform some analysis we need our different tables to be able to communicate so, I merged     queries. The merge allows for communication between both tables.




## Data Modeling
## Data Visualization and Analysis
## Insights
## Recommendations and Conclusions
