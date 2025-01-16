# Walmart-Sales-Analysis



![image](https://github.com/user-attachments/assets/55beb3af-61b9-4c03-9e0d-b052f247eb80)








## Project Overview:


This project aims to explore the Walmart Sales data to understand top performing branches and products, sales trend of different products, customer behaviour. The aims is to study how sales strategies can be improved and optimized.

**Purposes Of The Project**


The major aim of thie project is to gain insight into the sales data of Walmart to understand the different factors that affect sales of the different branches.

### About the Dataset
**Initial Dataset Fields :** Invoice ID, Branch, City, Customer type,	Gender,	Product line,	Unit price,	Quantity,	Tax 5%,	Total	Date,	Time,	Payment, cogs, gross margin, percentage, gross, income, Rating
![image](https://github.com/user-attachments/assets/c46736ec-fb12-4101-bc75-e1380519e71e)

**Newly Created Fields**
**>** ![image](https://github.com/user-attachments/assets/1c7aa838-3990-4350-93a5-5fbe02365956)
alter table walmartsalesdata add column Date_new date after date;

set sql_safe_updates = 0;
UPDATE walmartsalesdata 
SET 
    Date_new = STR_TO_DATE(date, '%Y-%m-%d');






## Some Business Questions and Answers
### 1. What is the most selling product line?
![image](https://github.com/user-attachments/assets/2dab3511-43bc-4239-acc4-63a28f55077f)
### 2. What is the total revenue by month?
![image](https://github.com/user-attachments/assets/bc80f806-841a-49b5-ac53-d4d49e9e49ce)
### 3. What product line had the largest revenue?
![image](https://github.com/user-attachments/assets/76fb8469-3408-4518-9e76-bc1df043ca8a)
### 4. What is the city with the largest revenue?
![image](https://github.com/user-attachments/assets/a3637f89-793a-47b7-afa7-aa1069668d76)
### 5. 



