# Walmart-Sales-Analysis



![image](https://github.com/user-attachments/assets/55beb3af-61b9-4c03-9e0d-b052f247eb80)








## Project Overview:


This project aims to explore the Walmart Sales data to understand top performing branches and products, sales trend of different products, customer behaviour. The aims is to study how sales strategies can be improved and optimized.

**Purposes Of The Project**


The major aim of thie project is to gain insight into the sales data of Walmart to understand the different factors that affect sales of the different branches.

### About the Dataset
**Initial Dataset Fields :** Invoice ID, Branch, City, Customer type,	Gender,	Product line,	Unit price,	Quantity,	Tax 5%,	Total	Date,	Time,	Payment, cogs, gross margin, percentage, gross, income, Rating
![image](https://github.com/user-attachments/assets/c46736ec-fb12-4101-bc75-e1380519e71e)

**Newly Created Fields :**

**> Date_new**

alter table walmartsalesdata add column Date_new date after date;

set sql_safe_updates = 0;
UPDATE walmartsalesdata 
SET 
    Date_new = STR_TO_DATE(date, '%Y-%m-%d');

**> time_of_date**

 alter table walmartsalesdata add column time_of_date varchar(20);

 SELECT 
    time,
    (CASE
        WHEN `time` BETWEEN '00:00:00' AND '12:00:00' THEN 'Morning'
        WHEN `time` BETWEEN '12:01:00' AND '16:00:00' THEN 'Afternoon'
        ELSE 'Evening'
    END) AS time_of_date
FROM
    walmartsalesdata;

**> day_name**

alter table walmartsalesdata add column day_name varchar (10);

UPDATE walmartsalesdata 
SET 
    day_name = DAYNAME(date_new);

**> month_name** 

alter table walmartsalesdata add column month_name varchar (10);

UPDATE walmartsalesdata 
SET 
    month_name = MONTHNAME(date_new);



## Some Business Questions and Answers

**BASIC ANALYSIS**
### 1. what are the unique branches, cities, and product lines are present in the data?
![image](https://github.com/user-attachments/assets/37ba5f21-ed39-428b-9ba0-45edd426283c)
![image](https://github.com/user-attachments/assets/fc061671-8cb0-455a-9993-06ab681d464f)
![image](https://github.com/user-attachments/assets/4495a770-bb46-493b-b4fc-8bc4327a1ebd)



### 2. What is the total revenue by month?
![image](https://github.com/user-attachments/assets/bc80f806-841a-49b5-ac53-d4d49e9e49ce)
### 3. What product line had the largest revenue?
![image](https://github.com/user-attachments/assets/76fb8469-3408-4518-9e76-bc1df043ca8a)
### 4. What is the city with the largest revenue?
![image](https://github.com/user-attachments/assets/a3637f89-793a-47b7-afa7-aa1069668d76)
### 5. 



