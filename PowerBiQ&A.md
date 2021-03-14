### 1.You manage a Power BI model that has two tables named Sales and Product. 
You need to ensure that a sales team can view only data that has a CountryRegionName value of Unites States and a ProductCategory value of Clothing. 

What should you do from Power BI Desktop? 
  
    * A. Add the following filters to a report.CountryRegionName is United States ProductCategory is Clothing
    * B. From Power BI Desktop, create a new role that has the following filters. [CountryRegionName] = "United States" [ProductCategory] = "Clothing" 
    * C. Add the following filters in Query Editor. CountryRegionName is United States ProductCategory is Clothing 
    * D. From Power BI Desktop, create a new role that has the following filter. [CountryRegionName] = "United States" && [ProductCategory] = "Clothing" 

Correct Answer: A 

References: https://docs.microsoft.com/en-us/power-bi/power-bi-how-to-report-filter 

### 2.You create a report in the Power BI service that displays the following visualizations: 
 A KPI that displays the count of customers 
 A table that displays the count of customers by country  A line chart that displays the count of customers by year 
 You need to receive an alert when the total number of customers reaches 10,000. 
 
 What should you do first?

    * A. Pin the line chart to a dashboard.
    * B. Pin the KPI to a dashboard. 
    * C. Embed the report into a Microsoft SharePoint page. 
    * D. Pin the report to a dashboard. 

**Correct Answer: D**

References: https://docs.microsoft.com/en-us/power-bi/service-dashboard-pin-tile-from-report 

### 3.You have an app workspace named Retail Store Analysis in the Power BI service. You need to manage the members that have access to the app workspace using the least amount of administrative effort. 
What should you do? 

* A. From the Office 365 Admin center, click Users.
* B. From the Power BI Admin portal, click Tenant settings. 
* C. From the Power BI Admin portal, click Usage metrics. 
* D. From the Office 365 Admin center, click Groups. 

**Correct Answer: D** 

References: https://docs.microsoft.com/en-us/power-bi/service-manage-app-workspace-in-power-bi-and-office-365 

### 4. Your organization has a Microsoft Office 365 subscription. 
When the users attempt to access the Power BI Service, they receive the error message shown in the exhibit. (Click the Exhibit button.) 
 
![alt text](/img/Question4_message.png)


You need to ensure that all the users can access the Power BI service. 
What should you do first? 

    * A. From the properties of each dashboard, modify the Share dashboard settings. 
    * B. From Microsoft Azure PowerShell, run the Set-MsolDomain cmdlet. 
    * C. Instruct each user to install Microsoft Office 2016. 
    * D. From Microsoft Azure PowerShell, run the Set-MsolCompanySettings cmdlet. 

Correct Answer: D  
References: https://docs.microsoft.com/en-us/power-bi/admin/service-admin-disable-self-service 

link2: https://docs.microsoft.com/en-us/powershell/module/msonline/set-msolcompanysettings?view=azureadps-1.0


### Scenario: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.

**You have a Power BI model that contains two tables named Sales and Date. Sales contains four columns named TotalCost, DueDate, ShipDate, and OrderDate. Date contains one column named Date.**

**The tables have the following relationships:**

    Sales[DueDate] and Date[Date]
    Sales[ShipDate] and Date[Date]
    Sales[OrderDate] and Date[Date]

The active relationship is on Sales[DueDate].

### Q. 5(a) You need to create measures to count the number of orders by [ShipDate] and the orders by [OrderDate]. You must meet the goal without duplicating data or loading additional data.

**Solution: You create a calculated table. You create a measure that uses the new table.**

Does this meet the goal?**

    * A.Yes

    * B. No

**Correct Answer: B**

### Q. 5(b) You need to create measures to count the number of orders by [ShipDate] and the orders by [OrderDate]. You must meet the goal without duplicating data or loading additional data. Solution: You create measures that use the CALCULATE, COUNT, and FILTER DAX functions. Does this meet the goal?

* A. Yes 
* B. No

**correct Answer: is  A**

 ### Q.5(C) You need to create measures to count the number of orders by [ShipDate] and the orders by [OrderDate]. You must meet the goal without duplicating data or loading additional data.
Solution: You create measures that use the CALCULATE, COUNT, and USERELATIONSHIP DAX functions.

Does this meet the goal?

    * A. Yes
    * B. No

**Correct Answer is A**

### Q6. You need to create measures to count the number of orders by [ShipDate] and the orders by [OrderDate]. You must meet the goal without duplicating data or loading additional data.

Solution: You create measures that use the CALCULATE, COUNT, and FILTER DAX functions.

Does this meet the goal?

A. Yes

B. No

**Correct Answer: A**

References:

https://msdn.microsoft.com/en-us/library/ee634966.aspx

https://msdn.microsoft.com/en-us/library/ee634825.aspx

https://msdn.microsoft.com/en-us/library/ee634791.aspx


### Q7. You need to create measures to count the number of orders by [ShipDate] and the orders by [OrderDate]. You must meet the goal without duplicating data or loading additional data.

Solution: You create two copies of the Date table named ShipDate and OrderDateGet. You create a measure that uses the new tables.

Does this meet the goal?

    * A. Yes

    * B. No

**Correct Answer: B**


### Scenarios:  This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution. After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.

**You have a user named User1. User1 is a member of a security group named Contoso PowerBI.**
 
**User1 has access to a workspace named Contoso Workspace.**

### Q 8. You need to prevent User1 from exporting data from the visualizations in Contoso Workspace.

Solution: From the Microsoft Office 365 Admin center, you remove User1 from the All Users security group.

Does this meet the goal?

A. Yes

B. No

**Correct Answer: B**

Note: We don;t need to delete that user from all groups, only removing him from Costoso group will give the solution.


### Q 9. Solution: From the Microsoft Office 365 Admin center, you modify the properties of Contoso PowerBI.

Does this meet the goal?

    * A. Yes

    * B. No

**Correct Answer: A** 

References:

https://docs.microsoft.com/en-us/power-bi/service-manage-app-workspace-in-power-bi-and-office-365


### Q. 10 Solution: From the PowerBI setting, you modify the Developer Settings.

Does this meet the goal?

    * A. Yes

    * B. No


**Correct Answer: B** 


## Scenario: You plan to embed multiple visualizations in a public website.

**You plan to embed multiple visualizations in a public website. Your Power BI infrastructure contains the visualizations configured as shown in the following table.**

![alt text](/img/Q11_visualImage.png)

### Q.11 Which two visualizations can you embed into the website? Each correct answer presents a complete solution.

NOTE:

Each correct selection is worth one point.

    * A. Visual 1

    * B. Visual 2

    * C. Visual 3

    * D. Visual 4

    * E. Visual 5


**Correct Answer: B, D ** 

References: https://docs.microsoft.com/en-us/power-bi/service-publish-to-web

link2: https://docs.microsoft.com/en-us/power-bi/collaborate-share/service-publish-to-web#limitations



## Scenario:  You have a Power BI dashboard that displays different visualizations of company sales.

You enable Q&A on the dashboard.
You need to provide users with sample questions that they can ask when using Q&A.

### Q 12 Which settings should you modify form the Power BI Settings?

    * A. Subscriptions

    * B. Workbooks

    * C. Dashboards

    * D. Datasets



**Correct Answer: D** 

References: https://docs.microsoft.com/en-us/power-bi/service-q-and-a-create-featured-questions

### Q.13.You have a Microsoft Excel spreadsheet that contains a table named Sales. You need to add the Sales table to a  Power BI dashboard as a tile.

How should you configure the tile?

    * A. From the Power BI service, import the data from the Excel workbook.

    * B. From Excel, publish the workbook to the Power BI service.

    * C. From the Power BI tab in Excel, pin the table.

    * D. From the Power BI service, upload the Excel workbook.

**Correct Answer is C.**

References: https://docs.microsoft.com/en-us/power-bi/publisher-for-excel


## Scenario: You are creating a report in Power BI Desktop.

You are consuming the following tables.

![alt text](/img/Q14_table.png)

**Date[Date] is in the mm/dd/yyyy format.** 

**Date[DateKey] is in the ddmmyyyy format.**

**Date[MonthNumber] is in the mm format.** 

**Date[MonthName] is in the mmm format.**

You create the report shown in the exhibit.

(Click the Exhibit button.)

![alt text](/img/Q14_Graph.png)

You need to ensure that the months appear in the order of the calendar.

### 14 How should you sort the MonthName column?

    * A. by MonthNumber

    * B. ascending

    * C. descending

    * D. by DateKey


**Correct Answer is A.**

References: http://ppmworks.com/sorting-month-names-chronologically-in-microsoft-power-bi-reports/


## Scenario: You plan to create a Power BI report. You have the schema model shown in the exhibit.

![alt text](/img/Q15_Schema.png)

The model has the following relationships:

Store to District based on DistrictID

Sales to Store based on LocationID

Sales to Date based on PeriodID

Sales to Item based on ItemID

You configure row-level security (RLS) so that the district managers of the stores only see the sales from the stores they manage. When the district managers view the Store by Items report, they see items for all the stores.

You need to ensure that the district managers can see items for the stores they manage only.

### Q.15 How should you configure the relationship from Sales to Item?

A. Select Assume Referential Integrity.

B. Change the Cardinality to One to Many (1:*).

C. Change the Cross filter direction to Both.

D. Change the Cardinality to One to one (1:1).


**Correct Answer is C.**

References: https://powerbi.microsoft.com/en-us/guided-learning/powerbi-admin-rls/


## Scenario: You use Power BI Desktop to create a visualization for a Microsoft SQL Server data source.


**You use Power BI Desktop to create a visualization for a Microsoft SQL Server data source.
You need to ensure that you can use R visualization.**

### Q 16. Which two actions should you perform?

Each correct answer presents part of the solution.

NOTE:

Each correct selection is worth one point.

    * A. Download and install Microsoft R Server.

    * B. Download and install RStudio Server on the computer that has Power BI Desktop installed.

    * C. Install SQL Server R Services on the server that runs SQL Server.

    * D. Enable R Scripting on the computer that has Power BI Desktop installed.

    * E. Download and install Microsoft R on the computer that has Power BI Desktop installed.


**Correct Answer is D,E.**

References
https://docs.microsoft.com/en-us/power-bi/desktop-r-visuals


## Scenario: You have a Power BI model that contains the following two tables:

**Sales(Sales_ID, sales_date, sales_amount, CustomerID)
Customer(CustomerID, First_name, Last_name)
There is a relationship between Sales and Customer.**

### Q.17 You need to create a measure to rank the customers based on their total sales amount.

Which DAX formula should you use?

   *  A. RANKX(ALL(Sales), SUMX(RELATEDTABLE(Customer), [Sales_amount]))

* B. TOPN(ALL(customer), SUMX(RELATEDTABLE(Sales), [Sales_amount]))

* C. RANKX(ALL(customer), SUMX(RELATEDTABLE(Sales), [Sales_amount]))

* D. RANK.EQ(Sales[sales_amount], Customer[CustomerID])


**Correct Answer is C**


References: https://msdn.microsoft.com/query-bi/dax/rankx-function-dax


## Scenario: You have a Microsoft SharePoint Online site named Sales. Your company has 1,000 sales users. All the sales users can access Sales.

**You create a report in an app workspace in the Power BI service. You embed the report into a page on the Sales site by using the Power BI web part.**

### Q.18 You need to ensure that all the sales users can view the report from the Sales site.

What should you do?

* A. Configure the Portal Site Connection for the Sales site.

* B. Enable anonymous access for the Sales site.

* C. Configure the app workspace for Premium capacity.

* D. Disable the Embed content in apps setting from the Tenant settings in Power BI.


**Correct Answer is C**

References: https://docs.microsoft.com/en-us/power-bi/service-embed-report-spo


## Scenario: You plan to deploy a Power BI app workspace that will be viewed by 10,000 users. You need to ensure that dashboard data can be updated every 30 minutes.

## Q.19 What should you do?

A. Assign each user a Power BI Pro license.

B. Store the dataset in Microsoft Azure Storage that uses the Premium storage tier.

C. Create the app workspace by using an account that is assigned a Power BI Pro license.

D. Configure the app workspace for Premium capacity.

**Correct Answer is D**

References: https://docs.microsoft.com/en-us/power-bi/service-premium


## Scenario: You have a Microsoft Excel 2016 workbook that has a Power Pivot model.

    The model contains the following tables:

    Product (Product_id, Product_Name)
    Sales (Order_id, Order_Date, Product_id, Salesperson_id, Sales_Amount)
    Salesperson (Salesperson_id, Salesperson_name, address)
    The model has the following relationships:

    Sales to Product
    Sales to Salesperson
    You create a new Power BI file and import the Power Pivot model.

### Q.20 You need to ensure that you can generate a report that displays the count of products sold by each salesperson.

What should you do before you create the report?

* A. Create a one-to-one relationship between Product and Salesperson.

* B. For each relationship, change the Cross filter direction to Both.

* C. For each relationship, change the Cardinality to One to one (1:1).

* D. Change a many-to-one relationship between Product and Salesperson.

**Correct Answer is B**

References: https://docs.microsoft.com/en-us/power-bi/desktop-create-and-manage-relationships


## Scenario: You have a Power BI model that contains the following two tables:

    Sales (Sales_ID, DateID, sales_amount)
    Date(DateID, Date, Month, Week, Year)
    The tables have a relationship.

### Q.21 You need to create a measure to calculate the sales for same period from the previous year.

Which DAX formula should you use?

* A. SUM(sales[sales_amount]) – CALCULATE(SUM(sales[sales_amount]), DATESYID(Date[Date]))

* B. CALCULATE(SUM(sales[sales_amount]), SAMEPERIODLASTYEAR(Date[Date]))

* C. SUM(sales[sales_amount]) – CALCULATE(SUM(sales[sales_amount]), SAMEPERIODLASTYEAR(Date[Date]))

* D. CALCULATEx(SUM(sales(sales_amount]), DATESYID(Date[Date]))

**Correct Answer is B** (answer c ie right)

### References:

    https://msdn.microsoft.com/en-us/library/ee634825.aspx

    https://docs.microsoft.com/en-us/power-bi/desktop-quickstart-learn-dax-basics

    https://msdn.microsoft.com/en-us/library/ee634972.aspx


## Scenario: You plan to develop a Power BI report that has a bar chart to display the number of customers by location.You have a table named Customer that has the following columns:

    CustomerID
    CustomerName
    Address
    City
    ProvState
    Country

**You need to allow users to drill down by location. The report will display the number of each customer by Country, and drill down to ProvState, and then to City.**

### Q.22 How should you configure the drill down in the bar chart?

* A. In the Legend field, add Country. In the Axis field, add ProvState at the top, followed by City.

* B. In the Value field, add Country at the top, followed by ProvState, and then City.

* C. In the Value field, add Country. In the Legend field, add ProvState at the top, followed by City.

* D. In the Axis field, add Country at the top, followed by ProvState, and then City.

**Correct Answer is D**

References: 
    https://docs.microsoft.com/en-us/power-bi/guided-learning/visualizatio ns#step-18

    https://docs.microsoft.com/en-us/power-bi/power-bi-visualization-drill-down


## Scenario: You have a table named Sales that contains sales data for the United States. A sample of the data in Sales is shown in the following table.

![alt text](/img/Q23_table.png)

### Q.23 When you attempt to create a map that shows SalesAmount by Zone, you discover that the map shows a bubble based on cities instead of states. You need to ensure that the map shows bubbles based on states.

What should you do?

* A. Add a column named Country that contains United States as the value.

* B. Add a column for longitude and a column for latitude.

* C. Select the Zone field. From the Modeling tab, change the Data Category.

* D. Select the Zone field. From the Modeling tab, change the Data Type.


**Correct answer is C**

References: https://docs.microsoft.com/en-us/power-bi/guided-learning/visualizations#step-5


## Scenario: You have two tables named CustomerVisits and Date in a Power BI model. You create a measure to calculate the number of customer visits. You use the measure in the report shown in the exhibit.

![alt text](/img/Q24_graph.png)

**You discover that the total number of customer visits was 60,000, and that there were only 5,000 customer visits in August.**

### Q.24 You need to fix the report to display the correct data for each month.

What should you do?

* A. Modify the measure to use the CALCULATE DAX function.

* B. Create a relationship between the CustomerVisits table and the Date table.

* C. Modify the measure to use the sum DAX function.

* D. Create a hierarchy in the Date table.

**Correct Answer is B**

References:

https://docs.microsoft.com/en-us/power-bi/desktop-create-and-manage-relationships

https://docs.microsoft.com/en-us/power-bi/desktop-tutorial-create-measures


## Scenario: You have the following tables. There is a many-to-one relationship from Subscriber to Date that uses Subscriber[StartDate] and Date[Date]. The Cross filter direction of the relationship is set to Single.

![alt text](/img/Q25_tabel.png)

### Q.25 You plan to create a column chart that displays the following two measures:

    Count of SubscriberID by Month based on the StartDate
    Count of SubscriberID by Month based on the EndDate
    What should you do before you create the measures?

A. Create an active one-to-one relationship from Subscriber[StartDate] to Date[Date].

B. Change the Cross filter direction of the active relationship to Both.

C. Change the active relationship for many-to-one.

D. Create an inactive many-to-one relationship from Subscriber[StartDate] to Date[Date].

**Correct Answer is B**

References:

https://docs.microsoft.com/en-us/power-bi/desktop-create-and-manage-relationships

### Q. 26. You have a Power BI report that displays a bar chart and a donut chart on the same page. The bar chart shows the total sales by year and the donut chart shows the total sale by category.

**You need to ensure that when you select a year on the bar chart, the donut chart remains unchanged.**

**What should you do?**

    * A. Edit the interactions from the Format menu.

    * B. Set a visual level filter on the bar chart.

    * C. Set a visual level filter on the donut chart.

    * D. Add a slicer to the page that uses the year column.

**Correct Answer is A**

References: https://www.excelguru.ca/blog/2016/11/23/visual-interactions-in-power-bi/

### Q. 27 You have a Power Pivot model that includes a KPI.

You need to create a visualization based on the Power Pivot model as shown in the exhibit.

(Click the Exhibit button.)

![alt text ](/img/Q27_graph.png)

Which type of visualization should you use?

A. matrix

B. KPI

C. multi row card

D. table

**Correct answer is A**
References: https://docs.microsoft.com/en-us/power-bi/visuals/desktop-matrix-visual

### Scenario: This question is part of a series of questions that use the same scenario. For your convenience, the scenario is repeated in each question. Each question presents a different goal and answer choices, but the text of the scenario is exactly the same in each question in this series.

**You have a Microsoft SQL Server database that has the tables shown in the Database Diagram exhibit.**


![alt text ](/img/Q28_tables.png)

You plan to develop a Power BI model as shown in the Power BI Model exhibit.

![alt text](/img/Q28_tabelmodel.png)

You plan to use Power BI to import data from 2013 to 2015.

Product Subcategory[Subcategory] contains NULL values.


You implement the Power BI model.

** Below questions are based on above Scenario**

### Q.28 You need to add a new column to the Product Subcategory table that uses the following formula.

    =if [Subcategory]=null then -NA- else [Subcategory]

Which command should you use in Query Editor?

* A. Conditional Column

* B. Column From Examples

* C. Invoke Custom Function

* D. Custom Column

**Correct Answer is A**

References: http://community.powerbi.com/t5/Desktop/if-then-else/td-p/117999


### 28 (b). You plan to use Power BI to import data from 2013 to 2015. Product Subcategory[Subcategory] contains NULL values.

You implement the Power BI model.
You need to create a hierarchy that has Category, Subcategory, and Product.

Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.

![alt text](/img/Q28B_dragdrop.png)

**Answer**

![alt_text](/img/Q28_B_Answer.png)

References:
https://intelligentsql.wordpress.com/2013/05/08/tabular-hierarchies-across-multiple-tables/ https://www.desertislesql.com/wordpress1/?p=1629

### Q.29 You need to add a measure to rank total sales by product. The results must appear as shown in the following table.

![alt text](/img/Q29_tableresult.png)

Which DAX formula should you use?

* A. Product Ranking = RANKX(ALL(Product), [SalesAmount],,Asc, Dense)

* B. Product Ranking = RANKX(ALL(Product), [SalesAmount],,DESC, Skip)

* C. Product Ranking = RANKX(ALL(Product), [SalesAmount],,DESC, Dense)

* D. Product Ranking = RANKX(Product, [SalesAmount],,DESC, Skip)

**Correct answer is C**

References: https://msdn.microsoft.com/en-us/library/gg492185.aspx



### 30. You need to create a measure of Sales[SalesAmount] where Product[Color] is Red or Product[Size] is 50.

Which DAX formula should you use?

![alt text](/img/Q30_options.png)

**Correct answer is C**

References: https://msdn.microsoft.com/query-bi/dax/filter-function-dax


### Q. 31 You add another table named Territory to the model. A sample of the data is shown in the following table.

![alt text ](/img/Q30_table.png)

You need to create a relationship between the Territory table and the Sales table.

Which function should you use in the query for Territory before you create the relationship?

* A. Table.Distinct

* B. Table.IsDistinct

* C. Table.ReplaceMatchingRows

* D. Table.RemoveMatchingRows

**Correct answer is A**

References:
https://msdn.microsoft.com/en-us/library/mt260775.aspx

### Q.32 You plan to add a table named Date to the model. The table will have columns for the date, year, month, and end of the last month, and will include data from January 1, 2013 to December 31, 2015.

The Date table and the Sales table will have a relationship.

Which DAX functions should you use to create the columns?

* A. CALENDARAUTO, YEAR, MONTH, and EOMONTH

* B. CALENDAR, YEAR, MONTH, and ENDOFMONTH

* C. CALENDARAUTO, YEAR, MONTH, and ENDOFMONTH

* D. CALENDAR, YEAR, MONTH, and EOMONTH

**Correct answer is D**

References:

https://msdn.microsoft.com/en-us/query-bi/dax/calendar-function-dax

https://msdn.microsoft.com/en-us/query-bi/dax/year-function-dax

https://msdn.microsoft.com/en-us/query-bi/dax/month-function-dax

https://msdn.microsoft.com/en-us/query-bi/dax/eomonth-function-dax


### Q.33 You have two Microsoft SQL Server database servers named SQLProd and SQLDev. SQLDev contains the same tables as SQLProd, but only a subset of the data in SQLProd.

**You create a new Power BI Desktop model that uses 120 tables from SQLDev.You plan to publish the Power BI file to the Power BI service.**

You need to connect the model to the tables in SQLProd. The solution must minimize administrative effort.

What should you do from Query Editor before you publish the model?

A. Create a new connection to SQLProd, and then import the tables from SQLProd.

B. Delete the existing queries, and then add new data sources.

C. Configure the Data source settings.

D. Edit the source of each table query.

**Correct answer is D**


### Q.34 You have a Power BI model that has a date table. A sample of the data shown in the following table.

![alt text](/img/Q34_table.png)

You need to add a column to display the date in the format of December 01, 2014.

Which DAX formula should you use in Power BI Desktop?

* A. FORMAT([Date], “MMM”) & ” “& FORMAT([Date], “DO”) & “, “& FORMAT([Date], “YYYY”)

* B. FORMAT([Date], “MM”) & ” ” & FORMAT([Date], “DO”) & “, ” & FORMAT([Date], “YYYY”)

* C. [Date].[Month] & ” ”  & FORMAT([Date], “D”) & “, ” & [Date].[Year])

* D. FORMAT([Date], “MMMM DO, YYYY”)

Refrence: https://docs.microsoft.com/en-us/dax/custom-date-and-time-formats-for-the-format-function


### Q 35. From Power BI Desktop, you create a query that imports the following table.

![alt text](/img/Q35_table.png)

What should you do?

* A. From the Format menu, click Trim.

* B. From the Extract menu, click Last Characters.

* C. From the Split Column menu, click By Delimiter.

* D. From the Extract menu, click Text After Delimiter.

**Correct Answer is D**

References: https://msdn.microsoft.com/en-us/library/mt798301.aspx

### Q. 36. You plan to create several datasets by using the Power BI service.

You have the files configured as shown in the following table.

![alt text](/img/Q36_table.png)

You need to identify which files can be used as datasets.

Which two files should you identify? Each correct answer presents part of the solution.

NOTE: Each correct selection is worth one point.

* A. Data 1

* B. Data 2

* C. Data 3

* D. Data 4

* E. Data 5

**Correct answer is B, D**

References: https://docs.microsoft.com/en-us/power-bi/connect-data/service-get-data-from-files

### Scenario:Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.

**After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.**

### Q.37 You have an app workspace that contains a report. The report contains sensitive data.

        You need to ensure that you can embed the report into a custom application that will be accessed by external users. The external users will NOT have a Microsoft Azure Active Directory user account or Power BI licenses.

        Solution: From Publish to web, generate an iFrame.
        Does this meet the goal?

* A. Yes

* B. No

**Correct answer is B**


### Q.38 Solution: Configure the app workspace to be read-only for members and to run in a shared capacity.

Does this meet the goal?

* A. Yes

* B. No

**Correct Answer si B**

Refrence: https://docs.microsoft.com/en-us/power-bi/service-premium-what-is



### Q.39. Solution: Purchase Power BI Premium P1, and then configure the app workspace to run in a dedicated capacity.

Does this meet the goal?

* A. Yes

* B. No

**Correct Answer is A**

References: https://docs.microsoft.com/en-us/power-bi/developer/embed-sample-for-customers


## Scenario: You have a Microsoft Excel workbook that is saved to Microsoft SharePoint Online. The workbook contains several Power View sheets.

You need to recreate the Power View sheets as reports in the Power BI service.

### Q.40 Solution: From Excel, click Publish to Power BI, and then click Export.

Does this meet the goal?

A. Yes

B. No

**Correct answer is B**

### Q.41. Solution: From the Power BI service, get the data from SharePoint Online, and then click Import.

Does this meet the goal?

    * A. Yes

    * B. No

**Correct answer is A**

References: 
https://docs.microsoft.com/en-us/power-bi/service-excel-workbook-files

https://docs.microsoft.com/en-us/power-bi/connect-data/service-publish-from-excel


### Q.42 Your company has several developers who plan to create custom solutions that will interact with the API for the Power BI service.

**Which three operations can the developers achieve by using the API? Each correct answer presents a complete solution.**

NOTE: Each correct selection is worth one point.

* A. Retrieve rows from a dataset

* B. Create a dataset

* C. Add rows to a dataset

* D. Refresh an imported dataset

* E. Add a member to a row-level security role

**Correct answer is A,B, C**

Reference: https://docs.microsoft.com/en-us/rest/api/power-bi/pushdatasets/datasets_postrows

Note: all the power BI developer APIs are availble in above link.

### Q.43. 

![alt text](/img/Q43_question.png)

What should you do?

* A. Create a calculated column that adds the % symbol to the values.

* B. From the Modeling tab, change the Data Type to Percentage.

* C. Edit the query of the data source and change the Data Type to Percentage.

* D. Create a measure that adds the % symbol to the values

**Correct answer is D**

### Q.44
![alt text](/img/Q44_Question.png)


You need to create a query that retrieves the Categories data and the Customers data.

Which type of source should you use?

* A. JSON

* B. Text/CSV

* C. OData Feed

* D. XML

**Correct answer si D**

### Scenario: You are importing sales data from a Microsoft Excel file named Sales.xlsx into Power BI Desktop. You need to create a bar chart showing the total sales amount by region.

**When you create the bar chart, the regions appear as expected, but the sales amount value displays the count of sales amount instead of the sum of sales amount each region.**

### Q.44 You need to modify the query to ensure that the data appears correctly.

What should you do?

* A. Delete the query, import the data into Microsoft SQL Server, and then import the data from SQL Server.

* B. In Query Editor, add a calculated column that totals the sales amount column.

* C. Change the Data Type of sales amount column to Numeric.

* D. Refresh the data model.

**Correct answer is C**


### Q.45 You create a KPI visualization in Power BI Desktop that uses the month as the trend axis.

    You discover that the data is not sorted by month.

    You need to change the sort order of the visualization.

What should you do first?

* A. Convert the visualization to a different type.

* B. Remove the trend axis from the visualization.

* C. Modify the visual level filters.

* D. Modify the drill through filters.

**Correct answer is B**

### Q.46. You have a Microsoft SQL Server Analysis Services (SSAS) cube that contains historical data.

In Power BI Desktop, you have the following query for the cube

![alt text](/img/Q46_query.png)

The query retrieves 25,499 records.

When you check the data warehouse that is the source of the cube, you discover that there are 26,423 records.

You need to ensure that the query retrieves all 26,423 records.

What should you do?

* A. From Query Editor, refresh all the data.

* B. Change the query to use Live connection mode.

* C. Delete the Remove Duplicates step.

* D. Add an Unpivot Columns step.

**Correct answer is C**
note: Source contains all the records but due to remove duplicates step data row have been removed.


### Q.47 You have a query that retrieves sales data. A sample of the data is shown in the following table.

![alt text](/img/Q47_table.png)

You need to ensure that the values in the Date column contain a date. Null values must be replaced with the date from the previous row.

What should you click on the Transform tab in Query Editor?

* A. Format, and then Clean

* B. Date, and then Earliest

* C. Fill, and then Down

* D. Replace Values, and then Replace Errors

**Correct answer is C**

### Q.48 You plan to use Power BI Desktop to import 100 CSV files. The files contain data from different stores. The files have the same structure and are stored in a network share. You need to import the CSV files into one table. The solution must minimize administrative effort.

What should you do?

* A. Add a folder data source and use the Combine Files command.
* B. Add a folder data source and use the Merge Queries command.
* C. Add a Microsoft Excel data source and use the Merge Queries command.
* D. Add text/CSV data sources and use the Append Queries command.

**Correct answer is A**

References:
https://docs.microsoft.com/en-us/power-bi/desktop-combine-binaries


### Q.49 You have the following two queries in Power BI Desktop:
    -> A query named Query1 that retrieves a table named SMB_Customers from a Microsoft SQL Server database
    -> A query named Query2 that retrieves a table named
    
Enterprise_Customers from an Oracle database
Both tables have the same columns.
You need to combine the data from SMB_Customers and Enterprise_Customers.

Which command should you use?
* A. Combine Files
* B. Merge Queries
* C. Merge Columns
* D. Append Queries


** Correctanswer is D**

### 50. You are creating a Power BI Desktop report that has several bar charts and a date slicer. You need to create a slide show that can be viewed from the Power BI service. Each slide must display the charts filtered for a different year.

What should you do before you publish the report?

* A. Configure report level filters, and then create groups that use the List group type.
* B. Configure drillthrough filters for each bar chart, and then select Selection Pane.
* C. Filter the bar charts by using the slicer, and then create bookmarks.
* D. Configure page level filters, and then create groups that use the Bin group type.

**Correct answer is C**

Reference: https://docs.microsoft.com/en-us/power-bi/desktop-bookmarks


### Q. 51 DRAG DROP -
    You create a report in Power BI Desktop.
    You need to embed the report into a Microsoft SharePoint Online site.
    Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.
Select and Place:

![alt text](/img/Q51_drop.png)

Asnwer:
![alt text](/img/Q51_dragAnswer.png)

References:
https://powerbi.microsoft.com/en-us/blog/integrate-power-bi-reports-in-sharepoint-online/

### Q.52 You have a Power BI app named App1. The privacy for the App1 app workspace is set to Private.

A user named User1 reports that App1 does not appear in the My organization AppSource. App1 appears in the My organization AppSource for your account.

You need to ensure that User1 sees App1 from the My organization AppSource.
What should you do?

    * A. From the app workspace, click Update app, configure the Access setting, and then click Update app.
    * B. From the app workspace, share the dashboard.
    * C. From the app workspace settings, add a member.
    * D. From the app workspace, click Update app, configure the Content settings, and then click Update app.

 **Correct answer is A**  

### Q.53 You have a sales report in an app workspace. The report displays a map of sales by location and a bar chart of sales by year. The report has a slicer to filter the data by year.

You need to create a dashboard that contains visualizations. The solution must ensure that you can use the slicer to filter the data by year.
What should you do?

    * A. Pin each visualization to the dashboard, and then add a web content tile.
    * B. Add a page level filter, and then pin each visualization to the dashboard.
    * C. Publish the app workspace.
    * D. Pin the report as a live page.

**Correct Answer : D**

References:
https://docs.microsoft.com/en-us/power-bi/service-dashboard-pin-live-tile-from-report 

### Q.54 A data analyst publishes several Power BI visualizations to a blog.
You discover that some of the visualizations contain data that is considered private by your company.
You need to prevent the visualizations from being published to the blog.
What should you do?

    * A. From the Power BI Admin portal, disable the Publish to web setting.
    * B. From the Power BI settings, delete the embedded codes.
    * C. From the Power BI Admin portal, disable the Share content with external users setting.
    * D. From the dashboard settings, modify the Share dashboard settings.

**Correct Answer is A**
References: https://docs.microsoft.com/en-us/power-bi/service-publish-to-web

### Q.55 You have an app workspace that contains two datasets named dataset1 and dataset2. Dataset1 connects to a Microsoft Azure SQL database. Dataset2 connects to a Microsoft Excel file stored in Microsoft OneDrive for Business.

You create a report named Report1 that uses dataset1.
You pin Report1 to a dashboard named Dashboard1.
You publish the app workspace to all the users in your organization.

You need to delete dataset2 from the app workspace.
What should you do first?

    * A. Delete Dashboard1.
    * B. Delete Report1.
    * C. Unpublish the app.
    * D. Configure the refresh settings for Dataset2.


**Correct Answer : C**

### Q.56 You create a report in the Power BI service.
You plan to provide external users with access to the report by publishing the report to a public blog.

You need to ensure that the report in the blog post will be updated as the data is refreshed.

What should you do in the Power BI service?

    * A. Publish the app workspace to the entire organization. In the blog post, use the URL of the app workspace.
    * B. Share the report. In the blog post, use the URL of the dashboard.
    * C. Publish the report to the web. In the blog post, use the embed code URL.
    * D. In the blog post, use the URL of the report.


**Correct Answer : C**

References:https://docs.microsoft.com/en-us/power-bi/service-publish-to-web


### Q.57 In the Power BI service, you create an app workspace that contains several dashboards. You need to provide a user named user1@contoso.com with the ability to edit and publish dashboards.

What should you do?

* A. Modify the members of the app workspace.

* B. Configure security for the dataset used by the app.

* C. Share the dashboard, and then modify the Access settings of the dashboard.

* D. From the app workspace, click Update app, and then configure the Access settings.

**Correct Answer is : A **

(Note:- I would say A because modifying the status of a member in the app workspace will enable him to edit or publish a dashboard or not.

For answer B :
- Sharing a dashboard does not enable the user to edit it [“When you share a dashboard or report, the people you share it with can view it and interact with it, but can't edit it.”] https://docs.microsoft.com/en-us/power-bi/service-share-dashboards
- As for the “Access Setting” of the dashboard you can modify users’ capabilities to :
o Read (Only)
o Read and Share
o Owner
o Remove the access
Indeed if you upgrade the specific user to owner, he will be able to edit the given dashboards but not the other dashboards (the question states “several dashboards”). As for the rest of the capabilities none allows the user to edit the dashboard.

To enable a user to edit and publish several dashboards he needs to be a member of the given workspace where the dashboards are.)

References: https://docs.microsoft.com/en-us/power-bi/service-manage-app-workspace-in-power-bi-and- office-365

### Q.58 You embed a Power BI report in a Microsoft SharePoint Online page.
A user named User1 can access the SharePoint Online page, but the Power BI web part displays the following error message: â€œThis content isnâ€™t available.â€
User1 is unable to view the report.

You verify that you can access the SharePoint Online page and that the Power BI report displays as expected.
You need to ensure that User1 can view the report from SharePoint Online.

What should you do?

    * A. Publish the app workspace.
    * B. Share the dashboard in the app workspace.
    * C. Edit the settings of the Power BI web part.
    * D. Modify the members of the app workspace.

**Correct Answer : D**

References: https://docs.microsoft.com/en-us/power-bi/service-embed-report-spo


### Q.59 You have a Power BI model that contains the following two tables:
    -> Assets (AssetID, AssetName, Purchase_DateID, Value)
    -> Date (DateID, Date, Month, Week, Year)

The tables have a relationship. Date is marked as a date table in the Power BI model.
You need to create a measure to calculate the percentage that the total assets value increased since one year ago.

Which DAX formula should you use?

* A. (sum(Assets[Value]) - CALCULATE(sum(Assets[Value]), SAMEPERIODLASTYEAR(â€˜Dateâ€™[Date])))/CALCULATE(sum(Assets[Value])), SAMEPERIODLASTYEAR(â€˜Dateâ€™[Date])))

* B. CALCULATE(sum(Assets[Value]), SAMEPERIODLASTYEAR(â€˜Dateâ€™[Date]))/ (sum(Assets[Value])

* C. CALCULATE(sum(Assets[Value]),DATESYTD((â€˜Dateâ€™[Date]))/ (sum(Assets[Value])

* D. (sum(Assets[Value]) - CALCULATE(sum(Assets[Value]), SAMEPERIODLASTYEAR(â€˜Dateâ€™[Date]))/sum(Assets[Value])


**Correct Answer is : D** (confusion answer should be C)

References:
https://msdn.microsoft.com/en-us/library/ee634825.aspx
https://docs.microsoft.com/en-us/power-bi/desktop-quickstart-learn-dax-basics
https://msdn.microsoft.com/en-us/library/ee634972.aspx

###  Q.59 You create a report in the Power BI service that displays the following visualizations:

    -> A KPI that displays the count of customers
    -> A table that displays the count of customers by country
    -> A line chart that displays the count of customers by year

You need to receive an alert when the total number of customers reaches 10,000.

What should you do first?
* A. Pin the line chart to a dashboard.
* B. Pin the KPI to a dashboard.
* C. Embed the report into a Microsoft SharePoint page.
* D. Pin the report to a dashboard.

**Correct answer is D**

References:
https://docs.microsoft.com/en-us/power-bi/service-dashboard-pin-tile-from-report


### Q.60 You have a Microsoft Excel spreadsheet that contains a table named Sales.You need to add the Sales table to a Power BI dashboard as a tile.

How should you configure the tile?

* A. From the Power BI service, import the data from the Excel workbook.
* B. From Excel, publish the workbook to the Power BI service.
* C. From the Power BI tab in Excel, pin the table.
* D. From the Power BI service, upload the Excel workbook.

**Answer : C**

References:
https://docs.microsoft.com/en-us/power-bi/publisher-for-excel



### Q.61 Scenario: HOTSPOT - Your company plans to use Power BI for 20 users in the sales department. The users will perform the following tasks:

    -> Access a published Power BI app.
    Modify reports in an app workspace.
    -> Share dashboards created in My Workspace.

You need to identify which Power BI licenses are required for the tasks. The solution must use the Power BI (free) license, whenever possible.

Which license should you identify for each task? To answer, select the appropriate options in the answer area.
NOTE: Each correct selection is worth one point.
Hot Area:

![alt text](/img/Q61_graph.png)

Answer:

![alt text](/img/Q61_answer.png)

References:
https://docs.microsoft.com/en-us/power-bi/service-create-distribute-apps https://docs.microsoft.com/en-us/power-bi/service-collaborate-power-bi-workspace

### Q. 62 DRAG DROP -
From Power BI service, you publish an app that contains one dashboard and one report. Q&A is enabled on the dashboard.
In Q&A, a user types the query count of clients and fails to receive any results. The user then types the query count of subscribers and receives the expected results.
You need to ensure that the user can use both queries to receive the same results.
Which four actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.
Select and Place:

![alt text](/img/Q62_image.png)

Answer: 6-5-3-4

![alt text](/img/Q62_answer.png)


### Q.63
![alt text](/img/Q63_image1.png)
**Correct answer is**
![alt text](/img/Q63_ans_image.png)

References: https://msdn.microsoft.com/query-bi/dax/dateadd-function-dax

### Q.64 You are creating a report in Power BI Desktop.
You are consuming the following tables.

![alt text](/img/Q64_image.png)


You have a new table named Fiscal that has the same schema as the Date table, but contains the fiscal dates of your company.
You need to create a report that displays the total sales by fiscal month and calendar month.

What should you do?

* A. Union Fiscal and Date as one table.
* B. Add Fiscal to the model and create a one-to-many relationship by using Date[Year] and Fiscal[Year].
* C. Add Fiscal to the model and create a one-to-one relationship by using Date[Year] and Fiscal[Year].
* D. Merge Fiscal into the Date table.


**Correct Answer : D**

References: https://docs.microsoft.com/en-us/power-bi/desktop-shape-and-combine-data


### Q.65 Your company has a security policy stating that proprietary data must not be transferred over the Internet. During a security audit, auditors discover that executives use the Power BI service for reporting. You need to recommend a solution to ensure that the company adheres to the security policy. What should you include in the recommendation?

* A. Microsoft SQL Server column encryption 
* B. Microsoft Azure ExpressRoute 
* C. a site-to-site VPN to Microsoft Azure 
* D. the on-premises gateway for Power BI

**Correct Answer is : B**

Explanation: https://docs.microsoft.com/en-us/power-bi/service-admin-power-bi-expressroute


### Q.66 You have a Microsoft SQL Server database that contains the following tables

![alt text](/img/Q66_table.png)

The following columns contain date information: 
    • Date[Month] in the mmyyyy format 
    • Date[Date_ID] in the ddmmyyyy format 
    • Date[Date_name] in the mm/dd/yyyy format 
    • Monthly_returns[Month_ID] in the mmyyyy format The Order table contains more than one million rows. 

The Store table has a relationship to the Monthly_returns table on the StoreID column. This is the only relationship between the tables. You plan to use Power B! Desktop to create an analytics solution for the data. End of repeated scenario. 

**You need to create a chart that displays a sum of Order[Order_amount] by month for the Order_ship_date column and the Order_date column. How should you model the data?**


* A. Add a second Date table named Ship_date to the mode. Create a many-to-many relationship from Date[Date_ID] to Order [Order_date] and a many-to-many relationship from Ship_date[DateJD] to Order[Order_ship_date]. 

* B. Add a second Date table named Ship_date to the model. Create a one-to-many relationship from Date[Date_ID] to Order [Order_date] and a one-to-many relationship from Ship_date[Date_ID] to Order[Order_ship_dateJ. 

* C. Create a one-to-many relationship from Date[Date_ID] to Order[Order_date] and another relationship from Date[Date_ID] to Monthly_returns[Date_IDJ. 

* D. Create a one-to-many relationship from Date[Date_ID] to Order[Order_date] and another relationship from Date[Date_ID] to Order[Order_ship_date].


**Correct answer is B**


### Q.66 (b) You plan to use Power BI Desktop to create an analytics solution for the data.
You are modeling the data in Power BI.
You need to import only a sample of the data from the Order table.
What are two possible ways to achieve the goal? Each correct answer presents a complete solution

* A. From Query Editor, create a custom column that uses a custom column formula.
* B. From Query Editor, add a SELECT statement that uses a WHERE clause to the source definition.
* C. In the Power BI model, create a calculated table.
* D. From Query Editor, filter the table by Order_date.
* E. From Query Editor, create a column by using Column From Examples.

**Correct asnwer is BD**


### Q.66 (c) You plan to use Power BI Desktop to create an analytics solution for the data.
You are modifying the model to report on the number of orders.
You need to calculate the number of orders.
What should you do?

* A. Create a calculated measure that uses the COUNTA(Order_ID) DAX formula.
* B. Create a calculated column that uses the COUNTA(Order_ID) DAX formula.
* C. Create a calculated column that uses the SUM(Order_ID) DAX formula.
* D. Create a calculated measure that uses the SUM(Order_ID) DAX formula.

**Correct answer is A**

### 66(D) You plan to use Power BI Desktop to create an analytics solution for the data.
You plan to create a chart that displays total Order[Order_amount] by Store[Name].
You need to modify the model to ensure that you can create the chart.
Which two actions should you perform? Each correct answer presents part of the solution.


* A. Create a relationship between the Order table and the Store table.
* B. To the Order table, add a measure that uses the COUNTA('Order'[Order_ID]) DAX formula.
* C. To the Order table, add a column that uses the RELATED('Store'[Store_ID]) DAX formula.
* D. To the Order table, add a measure that uses the COUNT('Order'[Order_amount]) DAX formula.


**Correct answer is : AC**

### 66(E) You plan to use Power BI Desktop to create an analytics solution for the data.
You need to create a relationship between the Monthly_returns table and Date[Date_ID].
What should you do before you create the relationship?

* A. In the Date table, create a new calculated column named Month_ID that uses the yyyydd format.

* B. In the Monthly_returns table, create a new calculated column named Date_ID that uses the ddmmyyyy format.

* C. To the Order table, add a calculated column that uses the RELATED(Monthly_returns[Month_ID]) DAX formula.

* D. To the Date table, add a calculated column that uses the RELATED(Monthly_returns[Month_ID]) DAX formula.

**Answer is B**

References:
https://docs.microsoft.com/en-us/power-bi/desktop-create-and-manage-relationships


### 66(F) You plan to use Power BI Desktop to create an analytics solution for the data.
You need to display the month as a three-letter abbreviation, followed by the year, such as jan2017.
You add a calculated column in Power BI.
Which DAX formula should you use for the calculated column? To answer, drag the appropriate values to the correct targets. Each value may be used once, more than once, or not at all. You may need to drag the split bar between panes or scroll to view content.

![alt text](/img/Q66_E_dragdrop.png)

**Answer**
![alt text ](/img/Q66_E_Answer.png)

References:
https://docs.microsoft.com/en-us/dax/concatenate-function-dax#example-concatenation-of-columns-with-different-data-types https://docs.microsoft.com/en-us/dax/custom-date-and-time-formats-for-the-format-function

### 66(g) The Store table has a relationship to the Monthly_returns table on the Store_ID column. This is the only relationship between the tables.
You plan to use Power BI Desktop to create an analytics solution for the data.
You need to create a relationship between the Order table and the Store table on the Store_ID column.
What should you do before you create the relationship?

* A. In the Order table query, use the Table.TrasformRows function.
* B. In the Store table query, use the Table.TrasformRows function.
* *. In the Store table query, use the Table.TrasformColumnTypes function.
* D. In the Order table query, use the Table.TrasformColumnTypes function.

**ANswer is C**


### Q.67 Note: This question is a part of a series of questions that present the same scenario.
 Each question in the series contains a unique solution that might meet the stated goals.
 Some question sets might have more than one correct solution, while others might not have a correct solution.

 After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen. 

 You have a query for a table named Sales. Sales has a column named CustomerID. The Data type of CustomerID is Whole Number. You refresh the data and find several errors. You discover that new entries in the Sales table contain nonnumeric values. You need to ensure that nonnumeric values in the CustomerID column are set to 0. Solution: From Query Editor, select the CustomerID column and click Remove Errors.

Does this meet the goal?

    * A. Yes 
    * B. No

**Correct Answer: B**

### Q.67(b). Solution: From Query Editor, open Advanced Editor and add the following query step.

![alt text](/img/Q67_B_question.png) 

Does this meet the goal?
A. Yes
B. No

**Correct answer is B**




### Q.68. You create an app workspace named Wingtip Sales. Wingtip Sales is configured as shown in the following exhibit

![alt text](/img/Q68_image.png)

Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic. NOTE: Each correct selection is worth one point

![alt text](/img/Q68_question.png)

Answer: 
![alt text](/img/Q68_answer.png)

### Q. 69 You plan to use Power BI Desktop optimized for Power BI Report Server to create a report.
 
The report will be published to Power BI Report Server. You need to ensure that all the visualization in the report can be consumed by users. Which three types of visualizations should you include in the report? 

Each correct answer presents part of the solution. NOTE: Each correct selection is worth one point.

    * A. bubble maps 
    * B. custom visuals 
    * C. R visuals 
    * D. breadcrumbs 
    * E. funnel charts

**Correct Answer: ABE**

Explanation:  References: https://docs.microsoft.com/en-us/power-bi/report-server/install-powerbi-desktop



### Q.70 You have a Microsoft Excel workbook that contains two tables. From Power BI, you create a dashboard that displays data from the tables.

You update the tables each day.
You need to ensure that the visualizations in the dashboard are updated daily.

Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.

NOTE. More than one order of answer choices is correct. You will receive credit for any of the correct orders you select.
Select and Place:


![alt text](/img/Q70_question.png)

**Answer**
![alt text](/img/Q70_answer.png)

References: https://docs.microsoft.com/en-us/power-bi/refresh-scheduled-refresh

##  Scenario: You have a Microsoft SQL Server database that contains the following tables.

![alt text](/img/Q70_tables.png)

The following columns contain date information:
    
    • Date[Month] in the mmyyyy format 
    • Date[Date_ID] in the ddmmyyyy format 
    • Date[Date_name] in the mm/dd/yyyy format 
    • Monthly_returns[Month_ID] 

in the mmyyyy format The Order table contains more than one million rows. The Store table has a relationship to the Monthly_returns table on the StoreJD column. This is the only relationship between the tables. 

You plan to use Power Bl Desktop to create an analytics solution for the data. End of repeated scenario. You are modeling the data in Power Bl. 

### Q.71 You need to import only a sample of the data from the Order table. What are two possible ways to achieve the goal? Each correct answer presents a complete solution.

* A. In the Power Bl model, create a calculated table. 
* B. From Query Editor, create a custom column that uses a custom column formula.
* C. From Query Editor, add a select statement that uses a where clause to the source definition.
* D. From Query Editor, create a column by using Column From Examples. 
* E. From Query Editor, filter the table by Order_date.

**Correct Answer is: C, E**

 ### Q.72. You plan to use Power BI desktop to create an analytics solution for the data. End of repeated scenario. You plan to create a chart that displays total Order [Order_amount] by Store [Name]. You need to modify the model to ensure that you can create the chart. Which two actions should you perform? Each correct answer presents part of the solution. NOTE: Each correct selection is worth one point.

* A. To the Order table, add a column that uses the RELATED(‘Store’ [Store_ID]) DAX formula. 
* B. Create a relationship between the Order table and the Store table. 
* C. To the Order table, add a measure that uses the COUNT (‘Order’[Order_amount]) DAX formula. 
* D. To the order table, add a measure that uses the SUM (‘Order’ [Order_amount]) DAX formula.

**Correct Answer is: AD**



### Q.73 You have a column named phone_number. The values in the columns are in one of the following formats: 

999-999-9999x123 1-999-999-9999x232 +1-999-999-9999x66x666 

The values after x in the phone-number column indicate the phone extension. You need to create a custom column in Query Editor that contains only the phone extensions. 

How should you complete the query? To answer, drag the appropriate values to the correct targets. Each value may be used once, more than once, or not at all. You may need to drag the split bar between panes or scroll to view content.

![alt text](/img/Q72_dragdrop.png)

**Answer**

![alt text](/img/Q73_answer.png)

### Q.74 You have an app workspace that contains a report. The report contains sensitive data. You need to ensure that you can embed the report into a custom application that will be accessed by external users. The external users will NOT have a Microsoft Azure Active Directory user account or Power BI licenses. Solution: Purchase Power BI Premium P1, and then configure the app workspace to run in a dedicated capacity. Does this meet the goal?

    * A. Yes
    * B. No

**Correct Answer: A**

References: https://docs.microsoft.com/en-us/power-bi/developer/embed-sample-for-customers


### Q.74 You have a Power BI model that has the following tables:
    ✑ Product (Product_id, Product_Name)
    ✑ Sales (Order_id, Order_Date, Product_id, Salesperson_id, Sales_Amount)
    ✑ Salesperson (Salesperson_id, Salesperson_name, address)

You plan to create the following measure.
    Measure1 = DISTINCTCOUNT(Sales[ProductID])
You need to create the following relationships:
    ✑ Sales to Product
    ✑ Sales to Salesperson
The solution must ensure that you can use Measure1 to display the count of products sold by each salesperson.

How should you configure the relationships? To answer, select the appropriate options in the answer area.


![alt text](/img/Q74_Graphmodel.png)

**Answer**
![alt text](/img/Q74_Answer.png)

Explanation: References: https://docs.microsoft.com/en-us/power-bi/desktop-create-and-manage-relationships 

### Q.75. You have an on-premises Power BI Report Server. You plan to create a report in Power BI Desktop and publish the report to the report server. Which data source should the report use?

* A. Microsoft Azure SQL Database 
* B. a Microsoft SQL Server database 
* C. a Microsoft SQL Server Analysis Services (SSAS) database 
* D. Microsoft Excel

**Answer is : C**

References: https://docs.microsoft.com/en-us/power-bi/report-server/quickstart-create-powerbi-report https://docs.microsoft.com/en-us/power-bi/report-server/connect-datasources


### Q.76 You have a Microsoft SQL Server database that has the tables shown in the Database Diagram exhibit

![alt text](/img/Q76_tableSchema.png)

You plan to develop a Power BI model as shown in the Power BI Model exhibit. (Click the Exhibit button.)

![alt text](/img/Q76_tablemodel.png)

You plan to use Power BI to import data from 2013 to 2015.
Product Subcategory[Subcategory] contains NULL values.
End of Repeated Scenario.
You are implementing the Power BI model.
You need to edit the Product Category query to match the desired Power BI model.
How should you complete the advanced query? To answer, drag the appropriate values to the correct targets. Each value may be used once, more than once, or not at all. You may need to drag the split bar between panes or scroll to view content.


![alt text](/img/Q76_dragdrop.png)

**Answer**
![alt text](/img/Q76_Answer.png)

References:
https://msdn.microsoft.com/en-us/library/mt260776.aspx
https://msdn.microsoft.com/en-us/library/mt260808.aspx


### Q.77 You have a Power BI model for sales data. You need to create a measure to calculate the year-to-date sales and to compare those sales to the previous year for the same time period. Which DAX function should you use?

* A. PARALLELPERIOD 
* B. SAMEPERIODLASTYEAR 
* C. DATESYTD 
* D. PREVIOUSYEAR

**Correct Answer is : C**

References: https://msdn.microsoft.com/en-us/library/ee634873.aspx


### Q.78 You have the following two tables: • Subscriber (SubscriberlD, Enroll mentDate, ServicePlan) • Date (Date, Month, Week, Year) There is a relationship between Subscriber [EnrollmentDate] and Date[Date]. You plan to create a KPI for the number of subscribers enrolled in the current year. You need to create a goal that is five percent more than the number of subscribers enrolled during the previous calendar year. How should you complete the DAX formula? 

![alt text](/img/Q78_dragdrop.png)

**Answer: : CALCULATE, COUNT, PREVIOUSYEAR**


References: https://msdn.microsoft.com/en-us/library/hh272049(v=sql.110).aspx https://msdn.microsoft.com/en-us/library/ee634770.aspx

### Q.79 You have three Power BI Desktop projects named Reportl.pbix, Report2.pbix, and Report3.pbix that have the following characteristics: • Report1.pbix contains a custom visualization. • Report2.pbix implements row-level security. • Report3.pbix connects to a Microsoft SQL Server database by using DirectQuery. Which reports support Publish to Web, and which reports can be published to Power BI Report Server? 

![alt text](/img/Q79_drapdrop.png)

**Answer**
![alt text](/img/Q79_Answer.png)

References:
https
://docs.microsoft.com/en-us/power-bi/service-publish-to-web#custom-visual
https://docs.microsoft.com/en-us/power-bi/report-server/row-level-security-report-server


#### Q. 80 You have a Power BI Desktop project that uses DirectQuery to access an on-premises Microsoft SQL Server database. From Power BI Desktop, you can query the database. When you publish the Power BI Desktop project to the Power BI service, the visualizations cannot display the data. What should you do to resolve the issue?

* A. Locate the published dataset for the project in the Power BI service and configure the data source credentials.
* B. Install the on-premises data gateway (personal mode) and republish the project. 
* C. Install the on-premises data gateway and configure a data source. 
* D. Configure a Microsoft Azure ExpressRoute connection between the on-premises network and the Power BI service

**Correct anser is C**

References:
https://docs.microsoft.com/en-us/power-bi/service-gateway-sql-tutorial

### Q.81 Your company has 1,000 users in a Microsoft Office 365 subscription.
A Power BI administrator named Admin1 creates 20 dashboards and shares them with 50 users.
You discover that a user named User1 can access all the dashboards.
You need to prevent User1 from accessing all the dashboards.
Solution: From the properties of each dashboard, you modify the Share settings

* A. Yes 
* B. No

**Answer is : B**


References:
http://radacad.com/dashboard-sharing-and-manage-permissions-in-power-bi-simple-but-useful

https://docs.microsoft.com/en-us/power-bi/service-admin-administering-power-bi-in-your-organization#how-do

### Q.82 You have a query for a table named Sales. Sales has a column named CustomerlD. The Data Type of CustomerlD is Whole Number. You refresh the data and find several errors. You discover that new entries in the Sales table contain nonnumeric values. You need to ensure that nonnumeric values in the CustomerlD column are set to 0. Solution: From Query Editor, select the CustomerlD column. Click Replace Errors... and enter a value of 0.

Does this meet the goal?

    * A. Yes 
    * B. No

**Correct Answer: A**


### Q.83 You need to create a measure to calculate a running total of TransactionQuantity.
![alt text ](/img/Q83_table.png)

How should you complete the DAX formula? To answer, select the appropriate options in the answer area.
NOTE: Each correct selection is worth one point

![alt text](/img/Q83_question.png)

**Answer:**

![alt text](/img/Q83_answer.png)

Explanation:
References: http://www.daxpatterns.com/cumulative-total/

### Q 84. You have the datasets shown in the following graphic.

![alt text](/img/Q84_question.png)





### Q.85.You need to create a measure named YTDPreviousSales that will be used in a table visualization. YTDPreviousSales must show the year-to-date (YTD) sales of the previous year for the same month. A sample of the desired data is shown in the following tabl

![alt text](/img/Q85_table.png)

How should you complete the measure? To answer, drag the appropriate values to the correct targets. Each value may be used once, more than once, or not at all. You may need to drag the split bar between panes or scroll to view content. NOTE: Each correct selection is worth one point

![alt text](/img/Q85_question.png)



**Answer**
![alt text](/img/Q85_answer.png)

References:
https://powerpivotpro.com/2016/01/year-to-date-in-previousprior-year/


### Q. 86 QUESTION 5 From the Home tab in Power BI Desktop, you click Enter Data and create a table named Sales that contains the following data

![alt text](/img/Q86_tables.png)

What causes the visualization to display four rows of data instead of six?

* A. the Data Category of Region 
* B. the Default Summarization on Region 
* C. the Default Summarization on Sales
* D. the Data Category of Sales

**Correct Answer is: B**

### Q.87 You have a query that uses a Microsoft Excel data source. The data source contains the following table.

![alt text](/img/Q87_tablepivoted.png)

You need the data to appear as shown in the following table.

![alt text](/img/Q87_tableunpivoted.png)

What should you do? To answer, select the appropriate options in the answer area. NOTE: Each correct selection is worth one point.

![alt text](/img/Q87_image.png)

**Correct Answer**

![alt text](/img/Q87_answerimage.png)

### Q.88 You have a query that retrieves data from a Microsoft Azure SQL database.
You discover that a column named ErrorCode has several values starting with a space character, and a column named SubStatus contains several non-printable characters.
You need to remove all the leading whitespaces from ErrorCode and all the non-printable characters from SubStatus. All other data must be retained.
What should you do on each column? To answer, select the appropriate options in the answer area.
NOTE: Each correct selection is worth one point.
Hot Area:

![atl text](/img/Q88_image.png)

**Correct Answer**
![atl text](/img/Q88_answerimage.png)

References:
https://msdn.microsoft.com/en-us/library/mt260494.aspx
https://msdn.microsoft.com/en-us/library/mt253328.aspx

### Q.87 You are creating a work schedule for a retail store. You have the following data from a query named Schedule.

![alt text](/img/Q89_question.png)

You add a matrix visualization, and then you add Employee to the rows and Scheduled to columns. Which DAX formula should you use to create the measure that will display the checkboxes? To answer, drag the appropriate values to the correct targets. Each value may be used once, more than once, or not at all. You may need to drag the split bar between panes or scroll to view content

![alt text](/img/Q89_drapdrop.png)

**Correct Answer**

![alt text](/img/Q89_answer_image.png)

### Q.90 You have a query named FactlnternetSales used by several Power BI reports. The query is shown in the exhibit. (Click the Exhibit button.)

![alt text](/img/Q90_image.png)

You plan to create a bar chart showing the count of sales by year that have a SalesAmount greater than $1,000. You need to create a measure that will be used in the bar chart. How should you complete the DAX formula? To answer, drag the appropriate values to the correct targets. Each value may be used once more than once, or not at all. You may need to drag the split bar between panes or scroll to view content. NOTE: Each correct selection is worth one point.

![alt text](/img/Q90_image1.png)

**Correct Answer**

![alt text](/img/Q90_ans_image.png)


### Q.91 You create a new app workspace. You add a user named Userl1 as a member of the workspace. Userl1 can edit content. You plan to create a report in an app workspace that uses data from a Microsoft Azure SQL database. You need to create the report. The solution must ensure that Userl1 can edit the report from Power BI Desktop and from powerbi.com. Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.

![alt text](/img/Q91_image.png)

**Correct Answer**

![alt text](/img/Q91_ans_image.png)


### Q.92 You have a Power BI model that contains tables named Sales and Date. Sales contains four columns named SalesAmount, OrderDate, SalesPerson, and OrderID.
You need to create a measure to calculate the last 12 months of sales. You must start from the last date a sale was made and ignore any filters set on the report.

How should you complete the DAX formula? 

To answer, drag the appropriate values to the correct targets. Each value may be used once, more than once, or not at all. You may need to drag the split bar between panes or scroll to view content.

![alt text](/img/Q92_dragdrop.png)

**Answer **

![alt text](/img/Q92_answer.png)


### Q.93 You have a table named Sales. A sample of the data in Sales is shown in the following table.

![alt text](/img/Q93_table.png)

**You create a stacked column chart visualization that displays ProductName by Date. You discover that the axis for the visualization displays all the individual dates. You need to ensure that the visualization displays ProductName by year and that you can drill down to see ProductName by week and day.**

What should you do first?

* A. Create a new table that has columns for the date, year, week, and day.
* B. Create a new hierarchy in the Sales table.
* C. Format the visualization and set the type of the X-Axis to Categorical.
* D. Configure a visual filter for the Date column that uses an advanced filte

**Answer is A**


### Q.94 You have a workspace that contains 10 dashboards. A dashboard named Sales Data from two datasets. You discover that users are unable to find data on the dashboard by using natural language queries. You need to ensure that the users can find data by using natural language queries. What should you do?

* A. From the settings of the workspace, modify the Language Settings. 
* B. From the properties of the dashboard, modify the Q&A settings. 
* C. From the Sales Data dashboard, modify the dashboard as a Favorite. 
* D. From the properties of the datasets, modify the Q&A and Cortana settings.

**Correct Answer is : D**


References: https://docs.microsoft.com/en-us/power-bi/service-q-and-a-direct-query#limitations-during-public-preview

### Q.95 You have a Power BI report in an app workspace. You plan to embed a report from the app workspace into a line-of-business application by using Power BI Embedded. Which information should you provide to the application developers?

* A. The application token and the report URL 
* B. The report URL and a user name 
* C. The app workspace name and the access key 
* D. The access key and the report ID

**Correct Answer is : C**

References: https://docs.microsoft.com/en-us/power-bi/developer/integrate-report


### Q.96 You plan to create a report in Power BI Desktop.
You have the following tables.

![alt text](/img/Q96_table.png)

You have a measure that uses the following DAX formula.
Total Sales = SUM('Sales'[SalesAmount])
You plan to create a report to display TotalSales by ProductCategory and ProductSubCategory.
You need to create a measure to calculate the percentage of TotalSales for each ProductCategory.
How should you complete the DAX formula? To answer, drag the appropriate values to the correct targets. Each value may be used once, more than once, or not at all. You may need to drag the split bar between panes or scroll to view content.


![alt text](/img/Q96_drapdrop.PNG)

**Answer is as below**

![alt text](/img/Q96_answer.png)

References: https://support.office.com/en-us/article/when-to-use-calculated-columns-and-calculated-fields-ca18d63a-5b6d-4

### Q.97 You have a user named User!. User1 is a member of a security group named Contoso PowerB1. User1 has access to a workspace named Contoso Workspace. You need to prevent User1 from exporting data from the visualizations in Contoso Workspace. 

    Solution (a): From the Power B1 Admin portal, you modify the Tenant settings.

    * A. Yes 
    * B. No
    **Correct Answer is : B**

    Solution(b): From the PowerBI setting, you modify the Developer Settings. Does this meet the goal?
    * A. Yes
    * B. No

    **Correct Answer is : B**


### Q.98 Your company has 1,000 users in a Microsoft Office 365 subscription. A Power BI administrator named Admin1 creates 20 dashboards and shares them with 50 users. You discover that a use name User1 can access all the dashboards. You need to prevent User1 from accessing all the dashboards. 

    Solution (a): From Microsoft Azure Active Directory, you remove the Power BI license from User1. Does this meet the goal?

    * A. Yes 
    * B. No

    **Correct Answer is : A**

    References: https://docs.microsoft.com/en-us/power-bi/service-admin-administering-power-bi-in-your-organization#how-do


    Solution (b): From the Office 365 Admin center, you remove the Power BI license from User1. Does this meet the goal?

    * A. Yes 
    * B. No

    **Correct Answer is : B**

    Solution (C): From the Power BI Admin portal, you modify the Dashboard settings.
    Does this meet the goal?

    * A. Yes
    * B. No

    **Correct answer is B**

    Solution(d): From the properties of each dashboard, you modify the Share settings.
    Does this meet the goal?
    * A. Yes
    * B. No

    **Correct answer is A**

### Q. 99 You have a table named Sales. Sales contains the data shown in the following table.
![alt text](/img/Q99_image.png)

You have the following measure. Total Sales This Year = SUM([Total Sales]) You plan to create a KPI to compare the current yearly sales to the previous year as shown in the exhibit. (Click the Exhibit button.)

![alt text](/img/Q99_image1.png)

**Correct Answer is Calculate and dateadd**

### Q.100 You plan to use Power BI Embedded to deliver reports in a web application.
You need to ensure that the reports display live data.

Which data source you should use?

    * A. Microsoft Azure Data Lake Store
    * B. Microsoft Azure Table Storage
    * C. Microsoft Azure HDInsight
    * D. Microsoft Azure SQL Database

**Correct Answer: D** (might be A)

Explanation/Reference:
References: https://docs.microsoft.com/en-us/power-bi/service-azure-sql-database-with-directconnect


### Q.101 You plan to create a dashboard in the Power BI service that retrieves data from a Microsoft SQL Server database. The dashboard will be shared between the users in your organization.
You need to ensure that the users will see the current data when they view the dashboard.
How should you configure the connection to the data source?

    * A. Deploy an on-premises data gateway (personal mode). Import the data by using the Import Data Connectivity mode.
    
    * B. Deploy an on-premises data gateway. Import the data by using the Import Data Connectivity mode.
    
    * C. Deploy an on-premises data gateway. Import the data by using the DirectQuery Data Connectivity mode.
    
    * D. Deploy an on-premises data gateway (personal mode). Import the data by using the DirectQuery Data Connectivity mode.

**Correct Answer: C**

Explanation/Reference:
References: https://docs.microsoft.com/en-us/power-bi/desktop-directquery-about#power-biconnectivity- modes


### Q.102 You have a Power BI report that is configured to use row-level security (RLS).

You have the following roles:

A manager role that limits managers to see only the sales data from the stores they manage.

A region role that limits users to see only the data from their respective region

You plan to use Power BU Embedded to embed the report into an application. The application will authenticate the users.

You need to ensure that RLS is enforced when accessing the embedded report.

What should you do?

    * A. In the access token for the application, include the user name and the role name.

    * B. In the access token for the application, include the report URL and the Microsoft Azure Active Directory Domain name.

    * C. From dev.powerbi.com/apps, register the new application and enable the Read All Reports API access.

    * D. From dev.powerbi.com/apps, register the new application and enable the Read All Groups API access.

**Correct Answer: A**

References: https://docs.microsoft.com/en-us/power-bi/developer/embedded-row-level-security###

### Q.103 You plan to use Power BI Desktop to create a report. The report will consume data from an onpremises tabular named SalesDB in Microsoft SQL Server Analysis Services (SSAS). The report will be published to the Power BI service.
You need to ensure that the report published to the Power BI service will access the current data in SalesDB.

What should you do?

    * A. Deploy an on-premises data gateway and configure the connection to SalesDB to use the Import Data Connectivity mode.

    * B. Deploy an on-premises data gateway and configure the connection to SalesDB to use the Connect live option.

    * C. Deploy an on-premises data gateway (personal mode) and configure to SalesDB to use the DirectQuery Data Connectivity mode.

    * D. Deploy an on-premises data gateway and configure the connection to SalesDB to use the DirectQuery Data Connectivity mode.

**Correct Answer: B**


References: https://docs.microsoft.com/en-us/power-bi/desktop-use-directquery

### Q.104 You have a table named Sales. A sample of the data in Sales is shown in the following table.
![alt text](/img/Q104_image.png)

You created a stacked column chart visualization that displays ProductName by Date.
You discover that the axis for the visualization displays all the individual dates.

You need to ensure that the visualization displays ProductName by year and that you can drill down to see ProductName by week and day.

What should you do first?

    * A. Configure a visual filter for the Date column that uses an advanced filter.

    * B. Create a new table that has columns for the date, year, week, and day.

    * C. Create a new hierarchy in the Sales table.

    * D. Format the virtualization and set the type of the X-Axis to Categorical.

**Correct Answer: B**

References: https://docs.microsoft.com/en-us/power-bi/power-bi-report-add-filter#add-a-filter-to-aspecific- visualization-aka-visual-filter

### Q.105 You have a customer table in Power BI Desktop. The customer table contains the columns as shown in the following table

![alt text](/img/Q105_table.png)

You need to create a custom column that hides the first three digits of the SSN. The values in the new column must have the xxx-99-9999 format.
How should you complete the Query Editor formula? To answer, drag the appropriate values to the correct targets. Each value may be used once, more than once, or not at all. You may need to drag the split bar between panes or scroll to view content.

![alt text](.img\Q105_dragdrop.png)

**Answer**

![alt text](/img/Q105_answer.png)

References:
https://msdn.microsoft.com/query-bi/m/text-replace
https://msdn.microsoft.com/en-us/query-bi/m/text-start


### Q.106 You have the report shown in the following exhibit.

![alt text](/img/Q106_Question.png)
Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic

![alt text](/img/Q106_image.png)

**Answer**
 New table, 0.5


### Q.107  HOTSPOT
You open the Power BI Admin portal as shown in the following graphic.

![alt text](/img/Q107_image.png)

All the app workspaces use the customer's capacity.
Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic.


![alt text](/img/Q107_question.png)

**Answer**

![alt text](/img/Q107_Answer.png)

References:
https://docs.microsoft.com/en-us/azure/power-bi-embedded/scale-capacity https://docs.microsoft.com/en-us/power-bi/developer/embed-sample-for-customers



### 108 You need to create a dashboard in the Power BI service to display data from a PubNub source.
What should you do?

* A. Add a Microsoft SQL Server Analysis Services (SSAS) data source that uses Connect live and create a report. Pin the report to a dashboard.
* B. Create an app workspace and publish the workspace to a dashboard.
* C. Add a Microsoft Azure SQL database data source that uses DirectQuery and create a report. Pin the report to a dashboard.
* D. Add a custom streaming data tile to a dashboard

**Correct answer is; D**


### Q. 109 Your company has a custom line-of-business application named SalesApp.
The developers of SalesApp want to push data into the Power BI service to create several visualizations.
You need to ensure that the developers can push the data from SalesApp to the Power BI service.
What should you do?

* A. Go to portal.azure.com and create a web app.
* B. Go to app.powerbi.com/apps and register an application.
* C. Go to app.powerbi.com/admin-portal and click Publish to web.
* D. Go to app.powerbi.com and create an app workspace.


**Correct naswer is : B**

References:
https://docs.microsoft.com/en-us/power-bi/developer/walkthrough-push-data-register-app-with-azure-ad

### Q.109 You have a property named FactInternetSales used by several Power BI reports. The query is shown in the exhibit. (Click the Exhibit button.)

![alt text](/img/Q109_questionImage.png)

You plan to create a bar chart showing the count of sales by year that have a SalesAmount greater than $1,000.
You need to create a measure that will be used in the bar chart.
How should you complete the DAX formula? To answer, drag the appropriate values to the correct targets

**Answer**
1.countrows 2.filter



## Q.110 ou have a Power BI report that is configured to use row-level security (RLS).
    You have the following roles:
    ✑ A manager role that limits managers to see only the sales data from the stores they manage
    ✑ A region role that limits users to see only the data from their respective region

**You plan to use Power BI Embedded to embed the report into an application. The application will authenticate the users.
You need to ensure that RLS is enforced when accessing the embedded report.**

What should you do?
* A. From dev.powerbi.com/apps, register the new application and enable the Read All Reports API access.
* B. In the access token for the application, include the user name and the role name.
* C. From dev.powerbi.com/apps, register the new application and enable the Read All Groups API access.
* D. In the access token for the application, include the report URL and the Microsoft Azure Active Directory domain name.

**Correct answer is; B**

Reference: https://docs.microsoft.com/en-us/power-bi/developer/embedded/embedded-row-level-security
 
### Q. 111 You are creating a report in Power BI Desktop that has two visualizations on a page as shown in the following exhibi

![alt text](/img/Q_111_question.png)

You need to ensure that when you click the bar of a country, only the values for that country are shown on the Revenue by Year and Manufacturer chart.

* A. Click the Revenue by Year and Manufacturer chart. On the Format tab, click Edit Interactions. On the Units by Country chart, click Filter.
* B. Click the Revenue by Year and Manufacturer chart. On the Format tab, click Edit Interactions. On the Units by Country chart, click Highlight.
* C. Click the Units by Country chart. On the Format tab, click Edit Interactions. On the Revenue by Year and Manufacturer chart, click Filter.
* D. Click the Units by Country chart. On the Format tab, click Edit Interactions. On the Revenue by Year and Manufacturer chart, click Highlight.


**Correct asnwer is C**

### Q.112 You plan to create a dashboard in the Power BI service that retrieves data from a Microsoft SQL Server database. The dashboard will be shared between the users in your organization.
You need to ensure that the users will see the current data when they view the dashboard.
How should you configure the connection to the data source?

* A. Deploy an on-premises data gateway. Connect to the data by using the Import Data Connectivity mode.

* B. Deploy an on-premises data gateway. Connect to the data by using the DirectQuery Data Connectivity mode.

* C. Deploy an on-premises data gateway (personal mode). Connect to the data by using the Import Data Connectivity mode.

* D. Deploy an on-premises data gateway (personal mode). Connect to the data by using the DirectQuery Data Connectivity mode.


**Correct answer is: B**


### Q.113 You plan to create a dashboard in the Power BI service that will retrieve data from a tabular database in Microsoft SQL Server Analysis Services (SSAS). The dashboard will be shared between the users in your organization.
The Analysis Services database has a DirectQuery connection to the SQL Server database that contains the source data.
You need to ensure that the users will see the current data when they view the dashboard.
How should you configure the connection to the data source?

* A. Deploy an on-premises data gateway. Connect to the data by using the Connect live option.

* B. Deploy an on-premises data gateway. Connect to the data by using the DirectQuery Data Connectivity mode.

* C. Deploy an on-premises data gateway (personal mode). Connect to the data by using the Connect live option.

* D. Deploy an on-premises data gateway (personal mode). Connect to the data by using the DirectQuery Data Connectivity mode.
 
**Correct asnwer is A**

### Q. 114 You open powerbi.com as shown in the following exhibit.

![alt text](/img/Q114_Image.png)
Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic.

![alt text ](/img/Q114_question.png)

**Answer**
![alt text](/img/Q114_answer.png)

References:
https://biinsight.com/data-classification-in-power-bi/


### Q.115 You create a new app workspace. You add a user named User1 as a member of the workspace. User1 can edit content.
You plan to create a report in an app workspace that uses data from a Microsoft Azure SQL database.
You need to create the report. The solution must ensure that User1 can edit the report from Power BI Desktop and from powerbi.com.
Which three actions should you perform in sequence? To answer, move the appropriate action from the list of actions to the answer area and arrange them in the correct order.

![alt text](/img/Q115_question.png)

**Answer**
![alt text](/img/Q115_answer.png)

References:
https://docs.microsoft.com/en-us/power-bi/desktop-report-lifecycle-datasets


### Q.116 You have the following tables

![alt text](/img/Q116_Table.png)

You need to create a new table that displays the top 10 customers by the total of SalesAmount.
How should you complete the DAX formula? To answer, select the appropriate options in the answer area.

![alt text](/img/Q116_question.png)

**Answer**
![alt text](/img/Q116_answer.png)

### Q.117 You plan to join a fact table named ActivityLog to a Date dimension named ActivityDate. The date value in ActivityLog is a datetime column named ActivityStart.
The date value in ActivityDate is a number column named DateID. DateID is in the YYYYMMDD format.
What should you do in the model before you create the relationship?

* A. Change the Data Type of ActivityStart to Date.
* B. Create a measure in ActivityLog that uses the FORMAT DAX function.
* C. Change the Data Type of DateID to Date.
* D. Create a calculated column in ActivityLog that uses the FORMAT DAX function.

**Correct answer is D**

### Q 118 You have a table in Power BI Desktop as shown in the following exhibit

![alt text](/img/Q118_table.png)

You need to resolve the error in row 3. The solution must preserve all the data.
What should you do?

* A. Change the Data Type of the Value column.
* B. Select the Key column, and then click Remove Duplicates.
* C. Change the Aggregate Value Function of the pivot.
* D. Select the Score column, and then click Remove Errors.

**Correct answer is C**

### Q.118 You have a query that uses a Microsoft Excel data source. The data source contains the following table.
![alt text](/img/Q118_image.png)

What should you do? To answer, select the appropriate options in the answer area.
NOTE: Each correct selection is worth one point.

![alt text](/img/Q118_question.png)

**Correct answer**

![alt text](/img/Q118_ans.png)

### Q.119 You attempt to publish a Microsoft Excel file to Power BI, and you receive the error message shown in the exhibit. (Click the Exhibit button.)

![alt text](/img/Q119_image.png)

The file is in c:\data\.
You need to ensure that you can publish the file to Power BI.
What should you do first?

    * A. Save the file in a Microsoft SharePoint document library.
    * B. Decrypt the workbook.
    * C. Add a digital signature to the workbook.
    * D. Set the file attributes to read-only.

    **Correct answer is B**

References:https://docs.microsoft.com/en-us/power-bi/service-publish-from-excel

### Q.120 You plan to use Power BI Desktop to create a report. The report will consume data from an on-premises tabular database named SalesDB in Microsoft SQL
Server Analysis Services (SSAS). The report will be published to the Power BI service.

You need to ensure that the report published to the Power BI service will access the current data in SalesDB.
What should you do?

    * A. Deploy an on-premises data gateway and configure the connection to SalesDB to use the Connect live option.

    B* . Deploy an on-premises data gateway and configure the connection to SalesDB to use the Import Data Connectivity mode.

    * C. Deploy an on-premises data gateway (personal mode) and configure the connection to SalesDB to use the DirectQuery Data Connectivity mode.

    * D. Deploy an on-premises data gateway and configure the connection to SalesDB to use the DirectQuery Data Connectivity mode.
 
 **Correct Answer is A**

 ### Q.121 You have two tables named Customer and Orders. A sample of the Data in Customer is shown in the following table.
 ![alt text](/img/Q121_image.png)

You must use Customer as the first table.
Which join kind should you use?

    * A. Right Anti
    * B. Right Outer
    * C. Left Anti
    * D. Left Outer
    * E. Inner

**Correct Answer is D**

### Q.122 You are configuring the relationships between the following tables.
![alt text](/img/Q122_table.png)

A customer can have multiple accounts. An account can only be associated to one customer. Each account is associated to only one insurance policy.
You need to configure the relationships between the tables to ensure that you can create a report displaying customers and their associated insurance policies.
How should you configure each relationship? To answer, drag the appropriate cardinalities to the correct relationships. Each value may be used once, more than once, or not at all. You may need to drag the split bar between panes or scroll to view content.

![alt text](/img/Q122_question.png)

**Answer**

    Relationship from InsurancePolicy to Account = One-to-one
    Relationship from Account to BridgeAccount = One-to-one
    Relationship from Customer to BridgeAccount = One-to-many


### Q.123 You have a Power BI Desktop project that has the model shown in the exhibit. (Click the Exhibit tab.)

![alt text](/img/Q123_image.png)

Customer Count is a measure that uses the CountRows function to calculate the number of customers.
You create a table visualization that displays ProductID, Product, and Customer Count.
When you view the table, you discover that Customer Count always displays the total number of customers instead of the number of customers who purchased the product.
You need to ensure that the table visualization displays the number of customers who purchased each product.
What should you do?


* A. Modify the table relationship between the Customers table and the Sales table to use a Cross filter direction of Both.
* B. Modify the Customer Count measure to use the COUNT function.
* C. Modify the Customer Count measure to use the COUNTX function.
* D. Modify the table relationship between the Products table and the Sales table to use a Cross filter direction of Both.

**Answer is D**

### Q.125 You have sales data in a spreadsheet named Sales.xlsx.
You need to provide a detailed sales report to several managers.
From the Power BI service, you create an app workspace named SalesWorkspace.
Which three actions should you perform in sequence next? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.

![alt text](/img/Q125_question.png)

**Answer**
![alt text](/img/Q125_answer.png)


### Q.126 You need to create a measure named YTDPreviousSales that will be used in a table visualization. YTDPreviousSales must show the year-to-date (YTD) sales of the previous year for the same month. A sample of the desired data is shown in the following table.

![alt text](/img/Q126_table.png)

How should you complete the measure? To answer, drag the appropriate values to the correct targets. Each value may be used once, more than once, or not at all. You may need to drag the split bar between panes or scroll to view content.

![alt text](/img/Q126_dragdrop.png)

**Answer**
![alt text ](/img/Q126_answer.png)

References:
https://powerpivotpro.com/2016/01/year-to-date-in-previousprior-year/


### Q.126 You create a dashboard that displays the results of a customer satisfaction survey.
You need to embed a tweet from your company's Twitter feed into the dashboard.
What should you do?

    * A. Edit the report and import a visualization from the marketplace. Pin the visualization to the dashboard.
    * B. Edit the report and import a visualization from a file. Pin the visualization to the dashboard.
    * C. To the dashboard, add a tile that uses a web content source.
    * D. To the dashboard, add a tile that uses a PubNub content source.

**Correct Answer is C**
 

### Q.127 You have a report in Power BI Desktop as shown in the following exhibit.
![alt text](/img/Q126_image.png)

Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic.
Note: Each correct selection is worth one point.

![alt text](/img/Q127_image1.png)
**Correct answer**
![alt text](/img/Q127_answer_image.png)


### Q.128 You have the following table named Location.
![alt text](/img/Q128_image.png)

The GeoCode column represents the country where each customer is located.
You create a map visualization as shown in the exhibit. (Click the Exhibit tab.)

![alt text](/img/Q128_image1.png)

You need to ensure that the map displays the country locations.
What should you do?

    * A. Replace the values in the GeoCode column with postal codes or zip codes.
    * B. Change the name of the GeoCode column to Country.
    * C. Change the name of the Location table to Country.
    * D. Change the Default Summarization of the GeoCode column.
    * E. Add a Geoportal column to the Location table.
    * F. Change the Data Type of the GeoCode column.

    **Correct Answer is B**

References: https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-map-tips-and-tricks   

### Q.129 DRAG DROP -
You have a Power BI model that contains a table named Sales. Sales has the following three measures:

✑ A measure named Total Sales Last Year that displays the sales from the previous calendar year. The current value is 32.89 million
.
✑ A measure named Total Sales This Year that displays the sales from the current calendar year. The current value is 11.69 million.

✑ A measure named Total Sales Difference that uses a DAX formula of Sales[Last Year] "" Sales[This Year].

You need to create the following visualization.

![alt text](/img/Q129_image.png)
NOTE: Each correct selection is worth one point.
Select and Place:

**Correct Answer**

![alt text](/img/Q129_ans_image.png)

https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-radial-gauge-charts

### Q.130 You are creating reports in Power BI Desktop. The model has the following tables.

![alt text](/img/Q130_image.png)

There is a relationship between the tables.

You plan to publish a report to the Power BI service that displays Order_amount by Order_date by Full_name.
You need to ensure that only the columns required for the report appear in Report View. The solution must minimize the size of the dataset that is published.

How should you configure the columns in Power BI Desktop? To answer, select the appropriate options in the answer area.
NOTE: Each correct selection is worth one point.

![alt text](/img/Q130_image1.png)

**Correct Answer**
![alt text](/img/Q130_img_ans.png)


### Q.131 You have a table that contains a column named Phone. The following is a sample of the data in the Phone column.
![alt text](/img/Q131_image.png)
.
How should you complete the Query Editor formula? To answer, select the appropriate options in the answer area.
NOTE: Each correct selection is worth one point.
Hot Area:
![alt text](/img/Q131_image1.png)

**Correct Answer**

![alt text](/img/Q131_image_ans.png)

### Q.132  This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
You have a Microsoft Excel workbook that is saved to Microsoft SharePoint Online. The workbook contains several Power View sheets.
You need to recreate the Power View sheets as reports in the Power BI service.

Solution: Copy the workbook to Microsoft OneDrive for Business. From Excel, click Publish to Power BI, and the click Upload.

Does this meet the goal?

    * A. Yes
    * B. No

 **Correct Answer is B**   

 ### Q.133 Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.

    You have a Microsoft Excel workbook that is saved to Microsoft SharePoint Online. The workbook contains several Power View sheets.
    You need to recreate the Power View sheets as reports in the Power BI service.
    Solution: From the Power BI service, get the data from SharePoint Online, and then click Connect.

Does this meet the goal?

    * A. Yes
    * B. No
 
**Correct Answer: B**

    NOTE:-We need to click "Import", not "Connect".
    "Import or connect to an Excel workbook from Power BI.

    1.In Power BI, in the navigation pane, click Get Data.
    2.In Files, click Get.
    3.Find your file. --SharePoint - Team Sites
    4.If your workbook file is on OneDrive or SharePoint - Team Sites, choose 
    Import or Connect.

Refference: https://docs.microsoft.com/en-us/power-bi/service-excel-workbook-files

### Q.134 You have a Power BI model that contains the following tables:
✑ Sales (Sales_ID, DateID, sales_amount)
✑ Date (DateID, Date, Month, week, Year)

The tables have a relationship. Date is marked as a date table in the Power BI model.

You need to create a measure to calculate the sales for the last 12 months.

Which DAX formula should you use?

A. CALCULATEx(SUM(sales[sales_amount]) DATESYTD (‘Date’ [Dat))

B. CALCULATE(SUM(sales[sales_amount]), SAMEPERIODLASTYEAR (‘Date’ [Date]))

C. SUM(sales[sales_amount])-CALCULATE(SUM(sales[sales_amount]), SAMEPERIODLASTYEAR(‘Date’[Date]))

D. SUM(sales[sales_amount])-CALCULATE(SUM(sales[sales_amount]),DATESYTD(‘Date’[Date]))

**Correct Answer is C**