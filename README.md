# Performance Report
![Performance_Report](https://github.com/lakunleoye/Performance_Report-_PowerBI_Project/blob/master/Performance%20Report.png)

## Introduction
I created a condensed, dynamic performance report that utilises SWITCH measures and conditional formatting to identify any challenges and potential growth areas for a madeup Plant Company (Plant Co.) .This project used Plant Sales Data obtaned from ![Mo Chen's github](https://github.com/mochen862/power-bi-portfolio-project) contains information about sales & orders, locations, product details, and customer details.

### Report File
The report file is available here ![Performance Report.pbix](https://github.com/lakunleoye/Performance_Report-_PowerBI_Project/blob/master/Performance%20Report.pbix)

### Skills used for the project
These are the Power BI skills used for the project:

**1.	Power Query (ETL)**

**2.	DAX and Measures**

**3.	Data Modelling**

**4.	Visuals**

### Datasets used for the project
The dataset used for the project is an excel file comprised of 3 different tables on individual tabs. The first table, Product FACT, is a sales invoice with columns like Product_ID, sales, quantities, price, cost of goods (COGS), date of the invoice, and Account_ID. Second is the Account table, which has information for each specific acount. The columns include country code, account_ID, master_ID, long. and lat., country, postal code, street name, and street number. The third is the Plant Hierachy table. It has columns like product family, product group, product name, product size, and product type.


I used Power Query to:

**1. Extracted the three afore mentioned tables from the project's excel file which can be found ![here](https://github.com/lakunleoye/Performance_Report-_PowerBI_Project/blob/master/Plant_DTS.xls)**


**2. I Tranformed the dataset by:**

-Amending some column titles

-Removing duplicates from unique identifier columns

-Renaming the tables (Plant_Hierachy was changed to Dim_product, Account to Dim_Account, and Plant_FACT to Fact_Sales).


**3. I loaded the transformed queries, setting the stage for subsequent analysis**


## Dashboard Build

### Data Modelling

I first used **DAX** to create the Dim_Date table.

![DAX_4_Dim_Date](https://github.com/user-attachments/assets/41011ee8-5e17-4ef4-ab8e-464e030fed41)


I also create a Slicer Value's table to be used for SWITCH measures.

![Slicer_Values_Table](https://github.com/user-attachments/assets/fc637eb0-485a-4177-9a4c-63954cccc155)


I created a data model by integrating the Fact_Sales, Dim_Account, Dim_Sales, and Dim_Date tables into one model.

I also create a relationships among the tables using the Account_id, Product_id, and Date columns.

![Data Modelling](https://github.com/user-attachments/assets/8f14005c-8b85-4288-88e5-c91aed13aebc)


