# Plant Company Performance Report
![Performance_Report](https://github.com/lakunleoye/Performance_Report-_PowerBI_Project/blob/master/Performance%20Report.png)

## Introduction
I created a condensed, dynamic performance report that utilises SWITCH measures and conditional formatting to identify any challenges and potential growth areas for a madeup Plant Company (Plant Co.) .This project used Plant Sales Data obtaned from ![Mo Chen's github](https://github.com/mochen862/power-bi-portfolio-project) contains information about sales & orders, locations, product details, and customer details.

### Report File
The report file is available here ![Performance Report.pbix](https://github.com/lakunleoye/Performance_Report-_PowerBI_Project/blob/master/Performance%20Report.pbix)

### Skills used for the project
These are the Power BI skills used for the project:

**1.	Power Query (ETL)**

**2.	Data Modelling**

**3.	DAX and Measures**

**4.	Visuals**

### Datasets used for the project
The dataset used for the project is an excel file comprised of 3 different tables on individual tabs. The first table, Product FACT, is a sales invoice with columns like Product_ID, sales, quantities, price, cost of goods (COGS), date of the invoice, and Account_ID. Second is the Account table, which has information for each specific acount. The columns include country code, account_ID, master_ID, long. and lat., country, postal code, street name, and street number. The third is the Plant Hierachy table. It has columns like product family, product group, product name, product size, and product type.


## Power Query (ETL)
I used Power Query to:

**1. Extracted the three afore mentioned tables from the project's excel file which can be found ![here](https://github.com/lakunleoye/Performance_Report-_PowerBI_Project/blob/master/Plant_DTS.xls)**


**2. I Tranformed the dataset by:**

-Amending some column titles

-Removing duplicates from unique identifier columns

-Renaming the tables (Plant_Hierachy was changed to Dim_product, Account to Dim_Account, and Plant_FACT to Fact_Sales).


**3. I loaded the transformed queries, setting the stage for subsequent analysis**


## Data Modelling

I first used **DAX** to create the Dim_Date table.

![DAX_4_Dim_Date](https://github.com/user-attachments/assets/41011ee8-5e17-4ef4-ab8e-464e030fed41)


I also create a Slicer Value's table to be used for SWITCH measures. The switch is among Gross Profit, Quantity, and Sales.

![Slicer_Values_Table](https://github.com/user-attachments/assets/fc637eb0-485a-4177-9a4c-63954cccc155)


I created a data model by integrating the Fact_Sales, Dim_Account, Dim_Sales, and Dim_Date tables into one model.

I also create a relationships among the tables using unique identifiers like the Account_id, Product_id, and Date columns.

![Data Modelling](https://github.com/user-attachments/assets/8f14005c-8b85-4288-88e5-c91aed13aebc)

## DAX and Measures

Build base measures (Gross Profit, Quantity, and Sales) that are needed for my SWITCH, "year till date" (YTD),and “previous year till date” (PYTD) measures.

I used DAX to:

1. Create base measures for Sales, Quantity, and Gross Profit.

![Base_Measures_Sales](https://github.com/user-attachments/assets/69276249-86ef-4a5d-a09f-b1e138fa12a5)

![Base_Measures_Quantity](https://github.com/user-attachments/assets/abaf0e34-b99f-4c86-85e7-4051b2a38ad1)

![Base_Measures_GrossProfit](https://github.com/user-attachments/assets/8e665d34-bec4-43fc-8254-e9955738e01b)


2.  Create YTD measures for Sales, Quantity, and Gross Profit.

![YTD_Measures_Sales](https://github.com/user-attachments/assets/c29e57bb-fcbd-460e-940e-b434308883ee)

![YTD_Measures_Quantity](https://github.com/user-attachments/assets/4ad2ad71-89e8-414e-b7cb-bf6914714645)

![YTD_Measures_GrossProfit](https://github.com/user-attachments/assets/24403c2e-a14d-40fd-98a9-06c4fa0684ea)


3. Create PYTD measures for Sales, Quantity, and Gross Profit.

![PYTD_Measures_Sales](https://github.com/user-attachments/assets/e8cd54ca-5cb7-497e-b1de-c4b9885d97cc)

![PYTD_Measures_Quantity](https://github.com/user-attachments/assets/d945ee78-5c28-4733-a5f6-c423b6125e64)

![PYTD_Measures_GrossProfit](https://github.com/user-attachments/assets/f98b4bb5-e47a-4ef9-854e-71af0e99d626)


4. Create SWITCH measures for YTD, PYTD, and the comparison of YTD and PYTD.

![Switch_YTD_Measures](https://github.com/user-attachments/assets/d1c4b8a1-811e-4d32-bd9e-15d4c700146d)

![Switch_PYTD_Measures](https://github.com/user-attachments/assets/ad894265-7ea4-4ca6-aea7-3db4399fb899)

![Switch_YTDvsPYTD_Measures](https://github.com/user-attachments/assets/43ba16ee-a6e1-4232-965d-2b2ca7b14c77)


5. Create Gross Profit percent measures

![GrossProfit_Percent](https://github.com/user-attachments/assets/1bc7f316-3bc2-479e-864e-e681bddaefcf)



## Visuals

I used:

1.	Card(new) visual for the Header Metrics and applied Conditional Formatting.

![Header Metrics](https://github.com/user-attachments/assets/58cc9aa1-e698-439a-9e37-e79e024a546f)


2.	Slicers for Values (sales, quantity, and gross profit) and Years.

![Slicers](https://github.com/user-attachments/assets/e8c07537-7422-4a4e-aa9b-103bb96b0405)


3.	Treemap visuals to see which countries have experienced highest decline (bottom 10) when comparing YTD and PYTD.

![Bottom_10_Country](https://github.com/user-attachments/assets/2b2fe2ad-a10a-4037-94ba-7b54bd8b74ca)


4.	Waterfall chart for YTD vs PYTD comparison measures. You can drill down on the Month, Country, and Products.

![YTD_vs_PYTD_Waterfall](https://github.com/user-attachments/assets/3da325fa-5cf6-45af-9c5d-819f771811b9)


5.	Line and Stack Column chart for the Values YTD (column) and PYTD (line), with Product Type as legend.

![Line and Stack Column](https://github.com/user-attachments/assets/743db053-c0a8-48c1-8f9c-0cc53ed98cbb)


6. Scattered chart for Gross Profit percent and SWITCH values to help segment the different accounts and gain insight into profitability. For example, focus can be placed on accounts that fall in the high-profitability, low-sales region to increase sales volume.

![Profititability_segmentation](https://github.com/user-attachments/assets/a2eea8ce-ca97-4449-973f-a49efd16dcd9)

   
## Conclusion
This dynamic performance report was created for Plant Company to identify challenges and potential areas for growth. It enables end-users to make informed decisions regarding their Sales and Gross Profit by time, location, and products, allowing them to concentrate on new strategies for market engagement.











