# Adventure Works Cycle Company-Report



## Summary

Adventure works cycle comapny is a fictional manufacturing company. This report is aimed at helping the company track Key Performance Indexes, compare regional outputs and identify high value customer. All in the bid to improve business performance. 


### Steps followed 

- Step 1 : The first dataset(territory lookup) file was loaded into Power query. The file contains information on the territory of operation of the buisness. 
- Step 2 : Power query editor was used to check that the data type for each column is adequate. Also, in the view tab, under Data preview section, "column distribution", "column quality" & "column profile" options were checked. Since by default, profile will Open only for 1000 rows, select "column profiling based on entire dataset". After examining the data and cleaning as neccessary, the dataset was loaded into power BI desktop.
- Step 3 :Another dataset called Product lookup was loaded into power query. Step 2 was repeated to check the quality of the data.Worthy to note that, the data type for product cost and product price columns was changed to currency.
- Step 4 : Product categories lookup and product subcategories lookup tables were loaded into power query. Step 2 was repeated.
- Step 5: In the product lookup table, all text before the second delimiter in product SKU column were extracted into a new column named SKU type. Zero values in Productstyle column were replaced with NA.
- Step 6: The Customer lookup table was loaded into power BI desktop. Checks as in Step 2 was repeated here. Note that the format menu was used to transform the text in the prefix, firstname and lastname columns and the three columns were merged to create a new column called Full Name.
- Step 7: Also in the Customer lookup table, the email column was duplicated and called it domain name. In domain name column, all text and characters except the domain name were removed, and the transform menu option was used to format the domain name column.
- Step 8: The calendar lookup table was loaded into power query editor. This table only has a single date column. Using the date tool in the transform menu, more columns were added to the table. After which, it was loaded to power BI desktop.
- Step 9: Sales data 2020-2022 tables were loaded and appended  in power query editor. Data quality checks were carried out as in Step 2.After which they were loaded into power BI desktop.
- Step 10: The Returns Data table was loaded into power query and data quality checks were carried out on the data set, then loaded into power BI desktop.
- Step 11:All tables(facts and dimensions) were connected using primary and foreign keys as shown:
![Screenshot 2024-08-03 071907](https://github.com/user-attachments/assets/c56aaf52-9a4c-4569-9340-1bd6f8d889ce)

- Step 12: On the Sales data table, the following DAX was used to create a new column called Quantity type.
![Screenshot 2024-08-04 182728](https://github.com/user-attachments/assets/fe8dba23-98ac-46f5-8328-eaa28717d5d9)

-Step 13: On the sales data table, DAX was used to pull the product price column from product lookup for easier calculation reference.
![Screenshot 2024-08-05 123133](https://github.com/user-attachments/assets/7b2e6f2f-4b3e-4946-96ab-7d8aa2125822)

- Step 14: A table was created called Measure Table which will contain our calculated measures.

- Step 15: A report of three pages was created for visualization as follows; Exec dashboard, Map, and Customers detail.

- Step 16: A measure called Total revenue was created to calculate the revenue generated by the buisness. 
![Screenshot 2024-08-05 112353](https://github.com/user-attachments/assets/3b35b316-315d-4009-8234-792e381aa1b8)

A card visual was used to display the outcome on the Exec dashboard.
![Screenshot 2024-08-05 112550](https://github.com/user-attachments/assets/abc56ea0-5973-4167-8938-b213a05f2187)

- Step 17: A measure called total cost was created with DAX
![Screenshot 2024-08-05 113103](https://github.com/user-attachments/assets/947c2e04-1041-4f70-8190-44b94f4e1710)

- Step 18: A total profit measure was created and card visual was used to show the outcome on the exec dashboard.
![Screenshot 2024-08-05 123603](https://github.com/user-attachments/assets/b11662b1-011e-4716-84ce-0faa7245301c)

![Screenshot 2024-08-05 123713](https://github.com/user-attachments/assets/e286f351-a037-42d4-9547-d6eca1a80c7e)

- Step 19:  A measure was created called Total orders in order to track exactly, the distinct order.
 ![Screenshot 2024-08-04 200725](https://github.com/user-attachments/assets/1d73db4b-11b5-44f1-a0ca-42aa5a08cf73)

 A card visual was used to show the outcome on the exec dashboard.
 ![Screenshot 2024-08-05 124014](https://github.com/user-attachments/assets/7cd1996f-9111-433f-8bb6-dd0f477532f6)

- Step 20: A Quantity returned measure was created using DAX function as seen.
![Screenshot 2024-08-04 193036](https://github.com/user-attachments/assets/88f44041-88ce-4cb1-a941-2b9414ffb8c9)

- Step 21: Another measure was created named Quantity sold as seen:
![Screenshot 2024-08-04 195119](https://github.com/user-attachments/assets/701cd18c-2e3a-4b5f-af71-e4f68ed6a1bf)

- Step 22: Measures generated in step 19 and 20 were used to create a new measure called Return rate, which was visualized using card on the exec dashboard.
![Screenshot 2024-08-05 124351](https://github.com/user-attachments/assets/7fa4583c-10dc-4b46-b9d5-4df8c8dd6237)

![Screenshot 2024-08-05 124516](https://github.com/user-attachments/assets/3a4488dd-95c5-4904-8893-5f02078f9874)

- Step 23: DAX was used to compare previous months for revenue, orders and return rate to see how well the buisness was performing. they were visualized using the Key Performance Index(KPI) on the exec dashboard.

![Screenshot 2024-08-05 124921](https://github.com/user-attachments/assets/cec52ef3-5230-4142-8271-c1add63f8838)

![Screenshot 2024-08-05 125127](https://github.com/user-attachments/assets/66283c61-9b0d-4f81-8581-ea1f4513ce53)

![Screenshot 2024-08-05 125357](https://github.com/user-attachments/assets/042403eb-b338-4321-9707-a39b81f4a89e)

![Screenshot 2024-08-05 125509](https://github.com/user-attachments/assets/fa80a0e6-344b-4208-a31d-480ef805fa60)

![Screenshot 2024-08-05 125626](https://github.com/user-attachments/assets/fbd5a2ae-3e17-4598-bf5a-6d432e1b6745)

![Screenshot 2024-08-05 125744](https://github.com/user-attachments/assets/27639e66-fe2a-4125-890e-9f37824058b2)

-Step 24:On the data view, the data category for the region,country and continent were changed on the territory table to geo-spatial categories.
- Step 25: A map visual was created with navigation buttons for the 4 countries where the buisness is located. This was displayed on the map page of the report.

![Screenshot 2024-08-05 130402](https://github.com/user-attachments/assets/9fe3d0b6-0b67-44b1-be36-97a082bf2ae1)

-Step 26: A measure was created called Total no of customer, and was visualized using card on the customers details page of the report.
![Screenshot 2024-08-04 201530](https://github.com/user-attachments/assets/b5558e7c-fa08-4cfb-92b4-2902fd3e9a16)

![Screenshot 2024-08-05 131706](https://github.com/user-attachments/assets/904180d8-1654-4ffb-88fd-081e9d441bee)

Step 27: A measure was created called Average revenue per customer and was visualized with card on Customers details page.
![Screenshot 2024-08-05 130810](https://github.com/user-attachments/assets/44f50004-c4e6-4239-ae72-e06707b6d086)

![Screenshot 2024-08-05 131936](https://github.com/user-attachments/assets/e28edb20-97b0-4ce2-be10-94e5f9904fe9)

- Step 28: A calculated column was created in the customer lookup table to group the income level of customer using DAX.
![Screenshot 2024-08-05 133610](https://github.com/user-attachments/assets/ad5bd7b2-be39-4625-a3b9-04c6bfef8149)

This was used to visualize the income level by orders in the customers details page of the report.

-Step 29: The report view contains 3 different reports. A dashboards for high level metrics (such as those contained in the Executive dashboard), metrics showing performance by company location and customers metrics.

Step 30: In the exec dashboard, 6 card visuals were used. While 4 were numeric displey of insights such as revenue, profit, orders and return rate, the other two displayed most purchased type and most returned product type. A line chart visual was used to show revenue generated over time. A table was used to show the top 10 products purchased with their associated metrics. A pie chart was used to show orders by product category.

# Snapshot of The Executive dashboard
![Screenshot 2024-08-05 161222](https://github.com/user-attachments/assets/abc4a26d-2e14-4619-9869-a995bfefaa42)

Step 31: The map dashboard showed the total orders by continents in a map visualization.

# Snapshot of The Map dashboard
![Screenshot 2024-08-05 141100](https://github.com/user-attachments/assets/9f370fc1-7cea-4f3e-b922-759e7697f0bb)

Step 32: The customers details dashboard shows top customer by order and revenue in card and table visuals, total customers and average revenue per customer in card visuals and line chart, total orders by income level and occupation in donut charts.
# Snapshot of the Customers details dashboard
![Screenshot 2024-08-12 145830](https://github.com/user-attachments/assets/09efc6b1-6a44-432b-93ba-39897729f814)


- On the far left of each report page are navigation buttons which can be used to navigate through the report pages and ![Screenshot 2024-08-05 190851](https://github.com/user-attachments/assets/0b1d87bc-b228-4282-a7fe-004e19394364) in the Exec dashboard is used to clear all filters.




# Insights
A 3 page report was created on ower BI desktop. The following inferences can be drawn from the report

### [1] Executive Dashboard

 1.1) At the time of this report, the buisness had generated $24.91m in revenue and $10.46m in profit. Total orders producing this revenue was 25.16k and the return rate was 2.17%.
The line chart can be used to check these metrics at any instance in time through the period from 2020-2022.

1.2) Month over month for revenue and returns are in a good place(positive progression by 3.31% and 1.18% respectively compare to the previous month). However, MoM of orders dropped by 0.88%.

1.3) Accessories is the most ordered product category making up 44.82% of the total orders.

1.4) Generally, the most purchased single product type is tyres and tubes and the most returned single product type is shorts. This can be filtered through different categories to ascertain the most returned or most ordered subcategory per category.

### [2] Map

2.1) This displayed the total orders by continent. North America had the highest business turnover as their total orders equal 11,724. This can be filtered through by countries to see each country's contribution to this metrics.

### [3] Customers details Dashboard

3.1) Overall, Mr Maurice Shaun's orders generated the most revenue for the buisness.

3.2) Adventure works had a total customer of 17,420 who generated an average of $1,431 per customer. The line chart visual can be used with the slicers of total customers and revenue per customers to filter through to ascertain revenue generated through the period.

3.3) Professionals with average income made the most orders. This can be filtered down as well.

3.4) Year slicers are also present here to check customer performance at any point through the three years period.

## Reference
- Chris D. and Aaron P., Maven Analytics, Microsoft Power BI desktop for Business Intelligence.

