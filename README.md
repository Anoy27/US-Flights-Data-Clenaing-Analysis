# US Flights Data Cleaning
This repository contains my analysis of US flights data from 1995 to 2016. This .txt dataset is full of errors and messy data. So, the primary focus is to clean the data and then analyze it.

## Project Overview:
I collaborated with a research team on a data cleaning project to prepare a US historical flights dataset for training an AI model. The dataset consisted of 1.2 million rows and 33 columns, encompassing 33 million data points. It contained detailed flight data, including transactional, temporal, geographical, and operational information. The primary goal was to ensure the dataset's integrity, usability, and compatibility for advanced AI-based predictive modeling.

## Dataset Details:
The dataset included the following key columns:

### Transaction Details:
Transaction_ID, Flight_Date, Airline_Code, Airline_Name, and Flight_Number.

### Flight Logistics: 
Origin_Airport_Code, Origin_Airport_Name, Origin_City, Dest_Airport_Code, Dest_Airport_Name, and Distance.

### Operational Timings: 
CRS_Dep_Time, Dep_Time, Wheels_off, Wheels_on, CRS_Arr_Time, Arr_Time, CRS_Elapsed_Time, and Actual_Elapsed_Time.
Delays: Dep_Delay, Arr_Delay.

The cleaning process addressed issues with null values, redundant information, incorrect formats, and other anomalies to optimize the dataset for machine learning workflows.

## Data Cleaning Process:
The following steps were undertaken to clean and transform the data:

### Column Usability Enhancements:
1. Edited column names for improved readability and usability.
2. Removed special characters from the Tail_Number column for standardization.

### Handling Missing and Redundant Data:
1. Dropped null values in critical columns like Dep_Time and Arr_Time since imputation was not feasible.
2. Eliminated redundant columns Cancelled and Diverted as they contained identical values (False/f).

### Consistency Checks:
Standardized values such as UNKNOWN and UNKNOW for consistency before handling nulls.

### Format Transformations:
1. Converted the Flight_Date column to the correct datetime format.
2. Transformed timing columns (CRS_Dep_Time, Dep_Time, etc.) into 24-hour time format.
3. Converted CRS_Elapsed_Time and Actual_Elapsed_Time from a raw minute format to an intuitive hour-minute format.
4. Cleaned the Distance column by removing the word “miles” and converting values to integers.

### Validation and Corrections:
1. Identified and corrected invalid or nonsensical entries in columns like CRS_Dep_Time, Dep_Time, Wheels_off, Wheels_on, etc.
2. Created a new column, Early_Dep, to capture flights that departed 2-5 minutes early by isolating negative delay values in Dep_Delay.
### Sorting and Final Adjustments:
Sorted the dataset in ascending order by Flight_Date to ensure temporal consistency.

## Outcome and Impact:
The cleaned and structured dataset enabled the research team to feed it into an AI model for predictive analysis seamlessly. By addressing anomalies, ensuring consistency, and enhancing readability, the dataset was transformed into a robust and reliable resource for training and validation. This project underscored the critical role of data cleaning in the success of AI and machine learning initiatives.
