# Performance Report
![Performance_Report](https://github.com/lakunleoye/Performance_Report-_PowerBI_Project/blob/master/Performance%20Report.png)

## Introduction
I created a condensed, dynamic performance report that utilises SWITCH measures and conditional formatting to identify any challenges and potential growth areas for a madeup company (Plant Co.) .This project used Plant Sales Data obtaned from ![Mo Chen's github](https://github.com/mochen862/power-bi-portfolio-project) contains information about sales & orders, locations, product details, and customer details.

### Report File
The report file is available here ![Performance Report.pbix](https://github.com/lakunleoye/Performance_Report-_PowerBI_Project/blob/master/Performance%20Report.pbix)

### Skills used for the project
These are the Power BI skills used for the project:

**1.	Power Query (ETL)**

**2.	DAX and Measures**

**3.	Data Modelling**

**4.	Visuals**

### Datasets used for the project
The dataset used for the project contains
I used Power Query to:

**1. Amend some column titles**

**2. Remove duplicates from unique identifier columns**

**3. Rename the tables (Plant_Hierachy was changed to Dim_product, Account to Dim_Account, and Plant_FACT to Fact_Sales).**

I also used DAX to create the Dim_Date table.

![DAX_4_Dim_Date](https://github.com/user-attachments/assets/41011ee8-5e17-4ef4-ab8e-464e030fed41)



### Dashboard Build

### Data Model
I created a data model by integrating the Fact_Sales, Dim_Account, Dim_Sales, and Dim_Date tables into one model.

I also create a relationships among the tables using the Account_id, Product_id, and Date columns.

![Data Modelling](https://github.com/user-attachments/assets/8f14005c-8b85-4288-88e5-c91aed13aebc)


