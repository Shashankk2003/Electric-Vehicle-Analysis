# Electricle-Vehicle-Dashboard

### Dashboard Link - [https://app.powerbi.com/links/epZUgNOokM?ctid=e14e73eb-5251-4388-8d67-8f9f2e2d5a46&pbi_source=linkShare]

## Problem Statement

The Electric Vehicle Population Analysis project aims to provide insights into the adoption and distribution of electric vehicles across the U.S. by analyzing a dataset of 150,000 entries. The project focuses on key metrics such as total vehicles, average electric range, and the distribution of BEV and PHEV vehicles.

Using Power BI, the project generates visualizations to illustrate trends like vehicle growth by model year, geographical distribution by state, and vehicle eligibility for Clean Alternative Fuel Vehicle (CAFV) incentives. The analysis will help stakeholders understand market trends, customer preferences, and the impact of incentives, enabling data-driven decisions for future electric vehicle strategies.


## KPI's Requirements

1. Total Vehicles: Total number of electric vehicles
2. Average Electric Range 
3. Total BEV Vehicles and % of Total BEV Vehicles
4. Total PHEV Vehicles and % of Total PHEV Vehicles


## Chart's Requirements

1. Total Vehicles by Model Year (From 2010 Onwards)
2. Total Vehicles by State
3. Top 10 Total Vehicles by Make
4. Total Vehicles by CAFV Eligibility
5. Top 10 Total Vehicles by Model


## Steps In Project

### Requirement Gathering/ Business Requirements
1. Data Connection
2. Data Walkthrough

### Data Cleaning / Quality Check
1. Data Modeling
2. Data Processing
3. DAX Calculations

### Data Visualization
1. Dashboard Lay outing
2. Charts Development and Formatting Dashboard / Report Development


## Requirement Gathering/ Business Requirements

The dataset for the Blinkit Data Analysis project, comprises 8,523 rows 
and 12 columns, focusing on sales data analysis. The columns included are Item Fat Content, Item Identifier, Item Type, Outlet Establishment Year, Outlet Identifier, Outlet Location Type, Outlet Size, Outlet Type, Item Visibility, Item Weight, Sales, and Rating. This dataset provides a comprehensive view of various attributes related to items and outlets, enabling detailed analysis.

![1](https://github.com/user-attachments/assets/59df1173-5b25-481e-a211-a2995f9eb2d0)


## Data Cleaning / Quality Check

Data cleaning involves identifying and correcting errors or inconsistencies in a dataset to improve its quality and usability.

## Column Quality

Column quality refers to the assessment of the validity, accuracy, and completeness of data within each column of a dataset. It helps identify errors, missing values, and inconsistencies that could impact the reliability of the analysis.

![2](https://github.com/user-attachments/assets/bcb4d31a-f763-48cc-83b6-755589e95e51)


## Column Profile

A column profile is a summary of the key characteristics and distribution of data within a specific column of a dataset. It includes statistics such as the number of entries, distinct values, errors, and the frequency of each value, helping to understand the content and structure of the data in that column.

![3](https://github.com/user-attachments/assets/277c0cf6-320f-4e8d-baa9-4320b7165003)


## Column Distribution

Column distribution refers to the breakdown of data within a specific column, showing the frequency and proportion of each unique value. It helps in understanding how different values are represented in the dataset, revealing patterns, trends, and outliers.

![4](https://github.com/user-attachments/assets/0481f406-d1a8-442d-8ccd-503bedc9c1f1)


## Standardizing Data

Standardizing data is a crucial step in data preprocessing, ensuring consistency and improving the accuracy of analyses. In this context, standardizing involves replacing specific abbreviations or variations with a common term. 


## DAX Calculation

DAX (Data Analysis Expressions) is a formula language used in Microsoft Power BI to create custom calculations and perform advanced data analysis. It helps users build formulas and expressions to aggregate, filter, and analyse data efficiently. DAX is essential for creating complex measures and calculated columns in data models.

### Total Vehicle
DAX can calculate the total number of vehicles by summing all entries in the dataset. This involves creating a measure that aggregates the total count of vehicles across various models and types in your dataset.
           
            Total Vehicles = DISTINCTCOUNT(Electric_Vehicle_Population_Data[DOL Vehicle ID])

### Average Vehicle Range
DAX can calculate the average electric range of vehicles by using a measure that averages the electric range column in the dataset. This provides insight into the typical electric range across all vehicles.

           Avg Range = CONCATENATE(FORMAT(AVERAGE(Electric_Vehicle_Population_Data[Electric Range]) ,"0.00"), "Km")

### Total BEV Vehicale
DAX can calculate the total number of Battery Electric Vehicles (BEV) by creating a measure that counts all entries classified as BEV in the dataset. This helps to identify the total number of BEVs in the electric vehicle population, providing key insights into the adoption of fully electric vehicles.

            BEV Vehicles = CALCULATE([Total Vehicles], Electric_Vehicle_Population_Data[Electric Vehicle Type] = "Battery Electric Vehicle (BEV)")

### % of BEV Vehicle
DAX can compute the percentage of Battery Electric Vehicles (BEVs) by creating a measure that divides the total number of BEV vehicles by the total number of vehicles in the dataset. This provides insights into the proportion of BEVs compared to the entire vehicle population.

            % of BEV = [BEV Vehicles] / [Total Vehicles]

### Total PHEV Vehicle
DAX can sum up the total number of Plug-in Hybrid Electric Vehicles (PHEVs) by creating a measure that aggregates the PHEV vehicle count from the dataset. This helps to determine the total number of PHEV vehicles in the dataset.

            PHEV Vehicles = CALCULATE([Total Vehicles], Electric_Vehicle_Population_Data[Electric Vehicle Type] = "Plug-in Hybrid Electric Vehicle (PHEV)")

### % of PHEV Vehicle
DAX can calculate the percentage of Plug-in Hybrid Electric Vehicles (PHEVs) by creating a measure that divides the total number of PHEV vehicles by the total number of vehicles in the dataset. This helps to determine the proportion of PHEV vehicles relative to the entire dataset.

            % of PHEV = [PHEV Vehicles]/[Total Vehicles]


## Data Visualization

Data visualization is the graphical representation of data, making complex information easier to understand and analyze. It transforms data into visual elements like charts, graphs, and maps, enabling users to identify patterns, trends, and insights that may not be immediately apparent in raw data. Effective data visualization is crucial for decision-making, as it allows stakeholders to quickly grasp the significance of data and make informed decisions.

## Visualizations and Insights

### Total Vehicles by Model Year (From 2010 Onwards)

Total Vehicles by Model Year illustrates 
the number of electric vehicles available each year, starting from 2010. This visualization helps track the growth and trends in electric vehicle adoption over time.

![5 (2)](https://github.com/user-attachments/assets/d6eff758-48dc-4474-8da0-634bccaf921c)


### Total Vehicle by State
Total Vehicles by State showcases the 
distribution of electric vehicles across different states. This visualization highlights regions with higher adoption rates, providing insights into geographic variations in electric vehicle presence.

![6](https://github.com/user-attachments/assets/fe7f4504-df62-4de3-99d1-1157c2fb7505)

### Top 10 Vehicles by Make

Top 10 Vehicles by Make highlights the leading electric vehicle manufacturers based on the total number of vehicles. This chart offers insights into the market dominance of specific brands and their share in the electric vehicle sector. 

![7](https://github.com/user-attachments/assets/7eb38657-fdba-46e9-8fe3-33b409ad33b9)

### Total Vehicles by CAFV Eligibility 

Illustrates the proportion of electric vehicles that qualify for Clean Alternative Fuel Vehicle (CAFV) incentives. This
visualization helps in understanding the impact of these incentives on vehicle adoption rates and the distribution of eligible vehicles. 

![8](https://github.com/user-attachments/assets/75dc15ae-b77a-4fe8-8090-0e0810969b87)

### Top 10 Vehicles by Model

Top 10 Vehicles by Model highlights the most popular electric vehicle models based on the total number of vehicles. This chart provides insights into consumer preferences and identifies which models are leading in the market. 

![9](https://github.com/user-attachments/assets/beb1f267-ed67-46c7-b038-85e5e16872e7)


### Snapshot of Analysis Dashboard

![10](https://github.com/user-attachments/assets/8f9076e9-83b9-4a8c-a727-6f45e5e368c6)


### Conclusion

In summary, the data analysis and visualization of electric vehicles offer valuable insights into the growth, distribution, and preferences within the market. The visualizations, including trends over time, geographical distribution, and market share by make and model, provide a comprehensive understanding of the electric vehicle landscape. By examining the total vehicles 
by model year, state, make, CAFV eligibility, and model, stakeholders can identify key trends, areas of high adoption, and popular models, which are crucial for making informed decisions about market strategies, product development, and policy initiatives. These insights enable a better grasp of the 
evolving electric vehicle sector, supporting strategic planning and fostering advancements in sustainable transportation.
