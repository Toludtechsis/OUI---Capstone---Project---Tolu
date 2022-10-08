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
First step was to acquire the dataset from the HR team then to begin the data cleaning process I imported the dataset into PowerBI which is the choiced tool for this analysis. The process of importing the dataset is called GetData to get on with data cleaning I used PowerQuery as a transformation tool to clean the data. When I brought in the dataset, I had two tables to work with.
### In PowerQuery I took the following steps
- First step in power query was to rename the tables to reflect the information I was working with.
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
- Created new Columns
- Executed unpivot to restructure a table within the dataset
- Renamed certain columns so that naming conventions are uniform across board.
- Due to the nature of the dataset provided in order to be able to perform some analysis we need our different tables to be able to communicate so, I merged     queries. The merge allows for communication between both tables.
- Created a new table called myMeasure to house measures to be created in my data model

<img width="922" alt="Oui capstonePBQ" src="https://user-images.githubusercontent.com/17475689/194579460-07e5c78d-83a3-459d-bbe8-821898b5d92b.PNG">


## Data Modeling
For the data model, there wasn't a lot of tables to work with because I had merge both tables reflecting only the needed columns within the first table which I called Employee table. Due to that fact loading the second table called the bonus table into the data model will cause redundancy which was why it was excluded from the data model.


<img width="355" alt="oui - model" src="https://user-images.githubusercontent.com/17475689/194582867-708dc48e-943b-41c9-9ab9-bfab26cf6159.PNG"> 

## Data Analysis and Visualization
Within the data report's fields pane, I created different measures using data analysis expressions (DAX) formulas. These measures will go on to become quite useful in my analysis. Measures allows us ask how data questions and derive answers, they are useful for the analysis of data.

### Measures Created
- Gender Classification Measures : To explore all the different gender classifications, Male , Female and Unspecified.

<img width="655" alt="Measure 1" src="https://user-images.githubusercontent.com/17475689/194586820-a0ae861a-edea-4c1b-862d-f81221189e14.PNG">


<img width="657" alt="gender measure 2" src="https://user-images.githubusercontent.com/17475689/194588464-f04cb1cf-e323-45ac-bda6-1e3b32127bb9.PNG">


<img width="651" alt="gender measure 3" src="https://user-images.githubusercontent.com/17475689/194589038-f2af38bb-c233-4740-a879-64b1bbd727e3.PNG">

- Total Aggregation Measures : These measures were used to calculate the summation of the Bonus, Salary and Take-home columns.

<img width="655" alt="total bonus" src="https://user-images.githubusercontent.com/17475689/194708445-0396749e-47fa-4996-a362-19be1a0a5499.PNG">

<img width="656" alt="salary" src="https://user-images.githubusercontent.com/17475689/194708528-5a629d59-66b0-4fca-95b7-69af7d79293b.PNG">

<img width="657" alt="takehome" src="https://user-images.githubusercontent.com/17475689/194708625-fc2874b2-b15d-42d0-b910-ee86479c5266.PNG">

- Minimum Employee Payout Requirement Measure: This measure was use to calculate the level of company compliance with the minimum pay requirement.

<img width="554" alt="MEpayout" src="https://user-images.githubusercontent.com/17475689/194712421-4f877db3-6376-4cc9-966e-9d4cfec4e45f.PNG">

### Visualization

- Gender Distribution in Palmoria Group
Palmoria Group boast of a total of 946 employees, out of which 465 are Males, 441 Females and 40 without gender specification.

<img width="268" alt="company gender1" src="https://user-images.githubusercontent.com/17475689/194713236-0511e743-4fcb-4033-90c9-53b3408e8e59.PNG">

 
Gender distribution across Regions and Departments

The gender distribution across the 3 regions indicates a higher number of male employees. 
Kaduna with the most number of employees at 361 employees having 50.42% male employees, 45.71% female employees and 3.88% unspecified gender employees.
Abuja has 335 employees having 47.46% male employees, 47.16% female employees and 5.37% unspecified gender employees.
Lagos has 250 employees having 49.6% male employees, 47.2% female employees and 3.2% unspecified gender employees.

<img width="146" alt="regons gender" src="https://user-images.githubusercontent.com/17475689/194713327-0dd47031-b718-4e00-bd96-6fddad6981cb.PNG">  

Palmoria Group has 12 departments in operation and within the  departments, 7 departments have a high number of male employees and 5 deparments have more Female employees.


<img width="178" alt="gnde department1" src="https://user-images.githubusercontent.com/17475689/194713429-8dac4a4b-0079-4919-8a53-e46b8d769421.PNG">

- Gender distribution by employee ratings
In comparison to the other gender, there were more Females in the highest rated categories. The analysis revealed that more employees fall into the average group, which is dominated by men, as well as the two lowest rated categorie and 46% of the total 39 employees who are not classified by gender are rated average.

<img width="246" alt="emp rating" src="https://user-images.githubusercontent.com/17475689/194717495-00643ddb-a34a-4972-b230-5ca91f9578b5.PNG">


- Minimum Employee Payout Requirement
The analysis reveals that only 35% of the company's employees is paid the required minimum amount, which is $90000 for all manufacturing enterprises.

<img width="340" alt="min Pay" src="https://user-images.githubusercontent.com/17475689/194717759-138d34bf-e6f9-4a3e-8722-3907deb26175.PNG">


- Salary Pay Structure in Departments
Accounting, Human Resources, and marketing all showed glaring gender pay disparities, with Unspecified getting more money, while the Business Administration and Product Management departments were more evenly split between the genders across the board.

<img width="189" alt="gendar salary dep" src="https://user-images.githubusercontent.com/17475689/194717615-7b90f136-a42c-48b3-b0ac-93e33acb9bc9.PNG">

## Insights

-	Gender distribution gap across the organization has a relatively close, with Male employees only 3% more than the Females employees and 4% of the work force either gender neutral or unspecified.

-	Female employees have a generally higher performance rating compared to their Male counterparts.

-	Male employees across the company have an higher pay with an average salary earning of  $75k compared to the $72k of their Female counterparts and employees with unspecified gender having the highest salary average of $78k.

-	Male employees across all the three regions earn more than their Female counterparts with Kaduna having the widest pay gap within the organization.

-	7 departments of the 12 departments has more Male employees while 5 departments have more Female employees.

-	Palmoria Group does not meet the minimum employee pay requirement set for manufacturing companies and only has a 35% compliance rate.

-	A total of 26 employees earn between 0k - 20k, 103 employees earn up to 30k, 105 employees earn 40k, 96 employees earn 50k, 99 employees earn 60k, 117 employees earn 70k, 108 employees earn 80k, 90 employees earn 90k, 105 employees earn up to 100k and 97 employees earn up to 120k


## Recommendations and Conclusions

-	The Management should set up structures to even out gender distribution across regions. 

- Departments with wide difference in gender distribution should be investigated to ascertain the reason and steps taken towards a more balanced distribution in those departments.

-	The gap in gender pay should be addressed especially where 	qualifications and duties are the same.

-	High rating employees should be properly acknowledged for their hard works. "Happy employees, makes a thriving organization",

-	The Management should take necessary steps required to meet the minimum employee pay threshold.


[View Dashboard Here](https://github.com/Toludtechsis/OUI---Capstone---Project---Tolu/blob/2e4f045e187b0ce5ab8b1ea8e59dc2ba4f7e3aac/Home.PNG)
[View Dashboard Here](https://github.com/Toludtechsis/OUI---Capstone---Project---Tolu/blob/2e4f045e187b0ce5ab8b1ea8e59dc2ba4f7e3aac/Home.PNG)
[View Dashboard Here](https://github.com/Toludtechsis/OUI---Capstone---Project---Tolu/blob/2e4f045e187b0ce5ab8b1ea8e59dc2ba4f7e3aac/Home.PNG)
