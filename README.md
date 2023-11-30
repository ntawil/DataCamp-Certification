# DataCamp Certifications
#### This project outlines my final project that I successfully completed to earn a certification through DataCamp as a Professional Data Analyst. The Certification required multiple choice technical exams and this project as a practical exam, intended to simulate a job scenario.

## Table of Contents
-[Project Overview](#project-overview)  
-[Data Source](#data-source)  
-[Tools](#tools)  
-[Data Cleaning and Preparation](#data-cleaning)  
-[Exploratory Analysis](#exploratory-analysis)  
-[Results and Insights](#results-and-insights)  
-[Recommendations](#recommendations)  
-[Limitations](#limitations)  
-[References](#references)  
### Project Overview
#### The setup for this project is simple. I am a Data Analyst at a fictional company "Pens and Printers" who primarily sells pens. My director assigned me a data analysis task based on a business goal to better understand our customers. By cleaning and analyzing customer data, my task was to create an actionable recommendation to the business stakeholders, for the ultimate goal of increasing profit.
### Data Source
> 1 dataset containing sales data on pens sold in a given year. Most notably, the sales_method field from the dataset notes how a customer was reached by Pens and Printers: email, phone call, or both.
### Tools
> I used only Python and packages such as pandas and NumPy to manipulate the data, and seaborn to graph and analye results.
### Data Cleaning
> Initial cleaning techniques included summarizing columns and understanding datatypes, finding null values and numeric outliers. Several columns had null values which I converted to 0's or removed (depend
### Exploratory Analysis
> I explored the dataset by graphing various fields and their relationships to other fields.
>  Once this was done, I noticed the dataset included sales where items were sold but no profit was recorded. This could theoretically happen for 2 reasons: data/accounting error or a discount/promotion. Since I didn't have that context and it was a proportionally small number of records with items sold and zero profit, I chose to keep these rows in the dataset instead of removing them as anamolies, as they were not substantially significant to summary statistics.
### Results and Insights
> #TODO
### Recommendations
> #TODO
> Future analysis would include exploring the relationship between revenue and the number of times a customer visited Pens and Printers website (represented by nb_site_visits), or if a new versus retained customer (represented by years_as_customer) was more/less likely to make a purchase.
### Limitations
> The most significant limitation of this project is the amount of context. Humans are not numbers, and we do not interact with the world in that way. Numbers and the analysis of them indicate patterns, not behavior
### References
> This project setup and dataset was provided by DataCamp for the purposes of demonstrating my skills and knowledge, attained from their course "Data Analysis with Python".
