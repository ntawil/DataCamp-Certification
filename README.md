# Sales Data Analysis of company "Pens and Printers": DataCamp Certification
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
#### The setup for this project is simple. I am a Data Analyst at a fictional company "Pens and Printers" who primarily sells pens. My director assigned me a data analysis task based on a business goal to better understand our customers. By cleaning and analyzing customer data, my task was to create an actionable recommendation to the business stakeholders, for the ultimate goal of increasing revenue.
In this scenario, a new product was released 6 weeks ago, and the company wants to evaluate sales method peformance over the 6 week market presence.

### Data Source
> 1 dataset containing sales data on pens sold in a given year. Most notably, the sales_method field from the dataset notes how a customer was reached by Pens and Printers: email, phone call, or both.

### Tools
> - Python with packages pandas and NumPy to manipulate the data
> - Seaborn to graph and analyze the results
> - DataCamp provided an online IDE for processing

### Data Cleaning
> Initial cleaning techniques included finding null values, summarizing columns and understanding datatypes, and numeric outliers. For example:
> - The years_as_customer field was meant to hold integer values representing the tenure of a given customer. The company was founded in 1984, so any customer older than 39 years (inclusive), is an anomoly and removed from the dataset.
> - The customer_id field is a unique identifier per customer, so I ensured the dataset contained no duplicates of this field.
> - The sales_method field should contain only 3 text options. Using a countplot, I could quickly visualize the counts of every unique value in this field, and noticed there were more than 3. These extras were simply mispellings of the intended 3 options, so a simple replace method fixed this.
> - Fields for revenue and nb_sold: the dataset included sales where items were sold but revenue = 0. This could theoretically happen for 2 reasons: data/accounting error or a discount/promotion. Since I didn't have that context and it was a proportionally small number of records with >1 items sold and zero revenue, I chose to keep these rows in the dataset instead of removing them as anamolies, as they were not substantially significant to summary statistics.

### Exploratory Analysis
> I explored the dataset by graphing various fields and their relationships to other fields. I chose fields to inspect based on business questions such as:
> - Who are our customers?
> - How do we sell to them?
> - How effective is each sales method?
> - How do we leverage our best sales methods to maximize revenue?
> Insights from these analyses can be found under [Results and Insights](#results-and-insights).
> 1. Defining the Customer Base
> - A histograph of years_as_customer shows the wide majority of customers acquired within 1-8 years. For a 38 year old company, this demonstrates recent growth.
> - I added a new field to the dataset, "region", which was a categorical value based on the customer's "state". For example, any customer from Minnesota or Michigan would be determined "midwest." Graphing a countplot for region, I identified the southwest to have less customers than the other 4 regions by an average ~54.89%.
> 2. Sales Methods
> - 3 unique sales methods: call, email, email+call
> - A countplot shows that 49% of sales are email only, 67% of all sales used email to some extent.
> - The sales team provided time estimations for each occurence of a sales method:
>   - mail = 0 min
>   - email+call = 10 min
>   - call = 30 min.
> By grouping each sale by sales method and taking the sum, a countplot shows total hours and total revenue per sales_method.
> 3. Sales Method Performance over 6 weeks
> - Narrowing in on revenue, I created a scatterplot of each sale grouped by weeks_since_launch (6 total groups), and colored each point by sales_method. This showed distinct revenue growth patterns for each sales_method individually, and as part of the overall sales strategy.
> - The average sale generated more revenue every week for each sales method, where email+call outperformed email and call respectively. Combining with previous explorations, I noted the average revenue per sales_method transaction:
>   - email = $90.00
>   - email + call = $158.70
>   - call = $45.90

### Results and Insights
> #TODO

### Recommendations
> #TODO
> Future analysis would include exploring the relationship between revenue and the number of times a customer visited Pens and Printers website (represented by nb_site_visits), or if a new versus retained customer (represented by years_as_customer) was more/less likely to make a purchase.

### Limitations
> The most significant limitation of this project is the amount of context. Humans are not numbers, and we do not interact with the world in that way. Numbers and the analysis of them indicate patterns, not behavior

### References
> This project setup and dataset was provided by DataCamp for the purposes of demonstrating my skills and knowledge, attained from their course "Data Analysis with Python".
