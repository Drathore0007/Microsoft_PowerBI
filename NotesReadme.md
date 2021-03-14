# Power BI


# Chapter2:  MOdeling and Visualizations

* List can be define in power query in curly braces, and values are seprated by comma,

        {1,2,3,4, true,"hello"}
    List can hold different datatypes and consucative value list can be define {1:10} which will give a list with value 1 to 100.

* Records: a records can be define in power query M in square braces []. 
    
        [quantity= 100, price= 50]

* Table: a table in M query language can be define as #table construct and columns can be define in a list without datatype.

        #table (
            { quantity, price},
            {
                {100,20},
                {200,40}

            }
            
        )

    We can define the datatyep for values as well as below
    
        #table (
            talbe tyep [ quantity= int64.type, price= int64.type],
            {
                {100,20},
                {200,40}

            }
            
        )




## DAX Language
Dax is excel query language used in power BI to create calculated columns and tables. 
    
* Dax is not cas-sensitive like M. 
* Strongly type language, not posible to mix different datatype in same column.

Dax Data types * :

* Decimal number
* Fixed Decimal
* Date
* Datetime
* Whole number
* Time
* Text
* True/Flase

Dax math Functions: 

![alt text](\img\DaxMathFunction.PNG)


* LOOKUPVALUE: A dax function to bring value by using many to one relation.

        Syntax:

        LOOKUPVALUE (
        table[result_column],
        table[search_column_1], <expression_1>,
        table[search_column_2], <expression_2>,
        <alternate_result>
        )
        
        Example:

        ProductDescription = LOOKUPVALUE( DimProduct[EnglishProductName], DimProduct[ProductKey], FactInternetSales[ProductKey])

Above customer dax fubction will add a prodcut description from DimProduct table to FactInternetSales

* GROUPINGVALUE: Used to craate a group column in table.

    ProductPriceGroup = IF ( 
        DimProduct[ListPrice] < 100 , "LOW" ,
        IF (DimProduct[ListPrice] < 1000 , "MEDIUM",
         "HIGH" 
         )
         )
    Above code create a product price group based on ListPrice.


    Grouping with SWITCH function:

        ProductPriceGroup=  SWITCH(
            TRUE(),
            DimProduct[ListPrice] < 100 , "LOW" ,
            DimProduct[ListPrice] > 100 , "MEDIUM" ,
            DimProduct[ListPrice] > 1000, "HIGH" ,
            "VERY HIGH"
        )

Calculate table function

* Filter: filter function filer the table reocrds base on condition and create a new table object.

        ExpensiveDimProduct = FILTER(DimProduct, 
            DimProduct[DealerPrice]>1000
            )  

    above table function will create table base on condition. where dealerprice is greater then 1000.

    Note: Multiple filter condition can be added in the filter with OR , AND logical operator.

    
        ExpensiveColorDimProduct = FILTER(DimProduct, 
            or (
                DimProduct[DealerPrice]> 100,
                DimProduct[color]='Red'
            )
            )

* ALL: function removes all the filters on table , columns and create anew table object.

        All color products = ALL(  
            DimProduct[EnglishProductName],  
            DimProduct[Class], 
            DimProduct[Color]
            )
     a new table is created with three columns mensioned above.

    

* CALCULATEDTABLE: Takes two parameters, a table and filter which needs to be apply.

        TABLE_CAL=  CALCULATETABLE(
            DIMproduct,
            DimProduct[DealerPrice]> 100,
            DimProduct[color]='Red'

        )


    We can use OR , AND logical operators for filters, but column used in OR must be same.

        --WRONG
        TABLE_CAL=  CALCULATETABLE(
            DIMproduct,
            OR(
                DimProduct[DealerPrice]> 100,
                DimProduct[color]='Red'
            )
        )
        --Correct
       TABLE_CAL=  CALCULATETABLE(
            DIMproduct,
            OR(
                DimProduct[DealerPrice]> 100,
                DimProduct[DealerPrice]< 1000,
            )
        )



* VALUE and DISTINCT: both perform same functionalyt but value return records with null also , Distinct does not.


* SUMARIZE: Is table function that sumarize data based on column provide and generate a new aggregated column.

        Syntax:
        table = SUMARIZE(
            TABLE,
            TABLE[col1]
            TABLE[col2]
            "sum of col3", sum(table[col3])
        )

        EXAMPLE:
        SumarizedTable = = SUMMARIZE(FactInternetSales, 
        DimProduct[EnglishProductName], 
        DimDate[CalendarYear], 
        "sum by year" , sum(FactInternetSales[SalesAmount]) )


* SUMRIZETABLE: Functionality is simmilar to SUMRIZE but here we do not need to add table name, also it return a blank row record.

        
        Syntax:
            table = SUMARIZE(
                TABLE[col1]
                TABLE[col2]
                "sum of col3", sum(table[col3])
            )

        EXAMPLE:
        SumarizedColumns = SUMMARIZECOLUMNS( 
            DimProduct[EnglishProductName], 
            DimDate[CalendarYear], "product soldin year" , sum(FactInternetSales[OrderQuantity]) )



* ADDCOLUMNS Adds a new column in table, generating a row context in the process.

    Function axcepts three parameters as TAble, column to add, and a column expression.

        Syntax: ADDCOLUMNS(
            table, 
        "EXPRESION COLUMN Name", 
        COlUMN EXPRESION
        )

        AddcolumnDate = ADDCOLUMNS( 
            all(DimDate[CalendarYear], DimDate[CalendarQuarter]), "year quarter sequence", 
            DimDate[CalendarYear]*4+ DimDate[CalendarQuarter])


* SELECTCOLUMN: Functionalty is similar to ADDCOLUMN but it doen not keep existing column for table in newly created table. only new columnt will be available.

        Syntax:
       SELECTCOLUMN = SELECTCOLUMNS( 
           ALL( DimProduct[ProductKey], DimProduct[EnglishDescription]), 
           "Qunatity SUM", SUM(FactInternetSales[OrderQuantity]))


* TOPN; Function return top row based on specific criteria( like order by).

        Syntax:
        TOPN(nnumber,
            VLAUE(tabel[col1]),
            column Expresions
        )

        EXAMPLE:
        TopCovidCases = TOPN(
            10, 
            VALUES(Covid19_confirmed_global[Country/Region]), 
            CALCULATE (SUM(Covid19_confirmed_global[Covid Case]))
            )




* CROSSJOIN: Crossjoin function allows you to create cartesian product between two or more tables.

        Syntax:
        Crossname = CROSSJOIN(
            VALUES('Table (2)'[Name1]) ,
            VALUES('Table (2)'[name2])
            )


* GENERATE: function accepts two table expression as parameters and allow to reference first row in table first when writing data in second one.

        Syntax: GENERATE (
            table expression 1,
            table expression 2
        )

        Example:
        Top3buyingCustomers = GENERATE( 
            DISTINCT(DimDate[CalendarYear]), 
            TOPN(
                3, 
                VALUES(DimCustomer[EmailAddress]), 
                CALCULATE(sum(FactInternetSales[SalesAmount]))
                ) 
            ) 

* GENERATEALL: works same as geneart but give all the records.


* GRNERATESERIES : You can grnrrate a table with one column      called value, contain a list of number with predefined increment.

    * These values need not to exist in data model. 
   * atleast two  argument required: start value, end value
   * If the start value is greater than the end value then result will be a table with no row.
   * optional third parameter specifies the increment, if ommitted the bydefault it is 1.
   1 to 5 = GENERATESERIES (1,5)

        
        
            Datetable = GENERATESERIES( 
                DATE(2020,1,1), 
                DATE(2020,5,6), 
                TIME(23,59,59))
        
        Function above will generate a table with single column value.


* CALENDAR: works same as GENERATESERIES DAX function but only for time series creation. Function creates a single table column.

    * takes two parameters, for start_date and END_DATE.
    * Increment happen on single day wise.

    Syntax:
    datetable = CALENDAR()


* CALENDARAUTO: Genearates a date table with single column, where it automatically picks with minimun year and max year from data modela to create date starting from  1 jan min(year from data model) and 31 dec max(year from data model).

    Note: suppose data model has min date as 2 july 2018 and max dat as 20 dec 2020 thans function will generate a column as start date from 1 jan 2018 and end date as 31 dec 2020.

    Syntax:
     datetable = CALENDARAUTO()

     
* ROW functions: Used to create a single row table in power query.

        Syntax: 
        Table = ROW(
            "Column name1"  cell_value,
            "Column name1"  cell_value,
            )

        EXAMPLE:
        table = ROW(
            "Sales ROWS" countrows(sale),
            "date rows" countrows(date)
        )


* UNION: Works similarly as APPEND
    * Combines more than two table vertically.
    * Name of column can not match but number of column in table should be same
    * UNOIN can be used to create common dimensions for serveral different tables.

    syntax: 
         Table1=
          union(
              ROW ("color",red,"value1",1)
              ROW ("color",blue,"value1",2) 
          )


 * INTERSECT : 

      intersect table=
          INTERSECT(
               
          union(
              ROW ("color",red,"value1",1)
              ROW ("color",blue,"value1",2) 
          ),
          
          union(
              ROW ("color",green,"value1",1)
              ROW ("color",blue,"value1",2) 
          )  
          )     

* EXCEPT : 

        Syntax:
        ExceptTable = EXCEPT(
               
          union(
              ROW ("color","red","value1",1),
              ROW ("color","blue","value1",2) 
          ),
          
          union(
              ROW ("color","green","value1",1),
              ROW ("color","blue","value1",2) 
          )  
          )  

* NATURALINNERJOIN : 
* NATURAL LEFT OUTER JOIN:

* DATATABLES : Allows you to create calculated tables with data you entered manually.

    It takes three parameter:- column name, data type, list of values, supported data types  by datatable - boolean, currency,datetime,double,integer,string


            Syntax Example:

            Dax_DATATABLE = DATATABLE( 
                "Type" , STRING,  
                "PRice" , currency, 
                "Quantity" , INTEGER , 
                {{"Shirt",20,2},
                { "pants",50, 4},
                {"Tshirt", 50, 20}
                } )



 ** Dax Datatable **
![alt text](.\img\DaxDatatable.PNG)


        syntax Example:

        Table Var = VAR Table1 = union(
              ROW ("color","red","value1",1),
              ROW ("color","blue","value1",2) ,ROW ("color","yellow","value1",2) )
          VAR Table2 =
          union(
              ROW ("color","green","value1",1),
              ROW ("color","blue","value1",2), ROW ("color","green","value1",1),
              ROW ("color","yellow","value1",2)
          )  return NATURALINNERJOIN(Table1, Table2) 
          

NOte: Creating a calendar with generate and Variables 

    CalendraTable = 
    var days = CALENDAR( date(2020, 1,1), date(2020,5,6)) 
        return GENERATE( days, 
                    var basesdate= [Date] 
                    var monthname = FORMAT(basesdate, "MMM") 
                    var monthNumber = MONTH(basesdate) 
                    var baseyear = YEAR(basesdate) 
                    var daydate = DAY(basesdate) 
                    
                return ROW( "todaydate" , daydate,          "monthname", monthname, "MonthNumber", monthNumber, "year", baseyear
                    )
                    )

### Measures

* Measures are used in some of the most common data analyses.    

* Simple summarizations such as sums, averages, minimum, maximum and counts can be set through the Fields well. 
* The calculated results of measures are always changing in response to your interaction with your reports, allowing for fast and dynamic ad-hoc data exploration
* If you want to use two columns in aggregation function you have to use iteration function
iteration function have suffix "X" amd are as follow:-
        SUMX
        AVERAGEX
        MINX
        MAXX

*  iterators generates row context, all row functions, so we can use RELATED function in measures.        

* Calculated columns are materialized so its consumes more disk space and RAM, on other hand measures are calculated at query time, which means measures recalculate its value everytime so its comsumes CPU resources.

    ![alt text](.\img\MeasureVsCalculatedColumns.PNG)

* Using calculate in measures:

    ![alt text](.\img\Calculate_In_Measure.PNG)


    Applying Filter condition in three different approach.

    ![alt text](.\img\CalculateMeasureFilter.PNG)


* ALLSELECTED: function works same as ALL but accept single argumnet as table or columns oject.


    Allselected = CALCULATE( 
        SUM(DimProductCategory[CategorySoldAmount]), 
        ALLSELECTED(DimProductCategory[CategorySoldAmount]))


* Opening Profit Dax functions.

    ![alt text](.\img\OpeningPRofitDax.PNG)

    Example can be seen as below.

    ![alt text ](.\img\OpeningProfitexampl.PNG)


    Other Date functions:
    ![alt text](.\img\DateFunctions.PNG)


        Syntex:
        OpeningMonthSales = OPENINGBALANCEMONTH( 
            sum(Salesdate[Sales Amount]), 
            Salesdate[OrderDate]) 

        Function above evalute Opening month sales for this month.
        same was ClossingBalanceMonth can be used to get Clossing month balance.

    Alse we can use calculate to get Privouce month salesas below.

        TotalSalesPMTD = CALCULATE( 
            sum(Salesdate[Sales Amount]), 
            DATEADD(Salesdate[OrderDate], -1, MONTH) )


    Below are also some importance date function
        
        * DateBetween: select a range betnween a specific interval.
        * Dateperiod: work smae as datebetween but receive 4 argumnet as below

            Profiit Total = CALCULATE (SUM(profit),
                DATEPERIODE( 'date', 
                max('date'), 
                -1 , 
                DAY/MONTH/QUARTER/YEAR))


* Using Inactive Relationship: We can use inactive relation between two table programaticlly by using USERELATIONSHIP keyword.

        Syntax: 
            Sales Amount = CALCULATE (
            SUM(factinternetsales[Sales Amount], 
            USERRELATIONSHIP(
                dimdate[datekey], 
                factinternetsales[InvoiceDateKey]))


* LASTNONBLANK and FIRSTNONBLANK:
this function are used to get first and last record for a day or month which satishfy the condition.

    Syntax: 
        
        FISTNONBLACK(table[col], expression)

    Example: 
    
        SalesOrders = CALCULATETABLE( 
            ALL( FactInternetSales[OrderDate], FactInternetSales[OrderQuantity], FactInternetSales[SalesAmount]), 
            
            LASTNONBLANK( FactInternetSales[OrderDate], FactInternetSales[OrderDate] ) )  
    
* Filter from Disconencted Tables: A filter can be pass from one to another table even if the relationship between two table in inactive.

    Syntax: CALCULATE(
        SUM(Target[sales Amoount]), 
        INTERSECT ( 
            VALUE(Target[order date]), 
            VALUE(DIMdate[date])) 
        )

    Note: INTERSECT function is used to use inactive relation between two table.

    use intersect on multiple column

        [Filtered Measure] :=

        CALCULATE (
            <target_measure>,
            INTERSECT (
                ALL (
                    <target_granularity_column_1>, 
                    <target_granularity_column_2>
                ),
                SUMMARIZE (
                    <lookup_table>
                    <lookup_granularity_column_1>
                    <lookup_granularity_column_2>
                )
            )
        )

    Same way we can use a TREATAS function and multi column virtual filter can be pass.

* TREATAS: function used to create a virtual relatoinship from one to other table.

    Syntax: 
    
        [Filtered Measure] :=
        CALCULATE (
            <target_measure>,
            TREATAS (
                SUMMARIZE (
                    <lookup_table>
                    <lookup_granularity_column_1>
                    <lookup_granularity_column_2>
                ),
                <target_granularity_column_1>,
                <target_granularity_column_2>
            )
        )

    Reference link: https://www.sqlbi.com/articles/propagate-filters-using-treatas-in-dax/


# Visualizations

### Bar Chart :
### There are 6 variant of bar chart:-

*  Stacked Bar Chart 
*  Stacked column chart   
*  Clustered bar chart
*  Clustered column chart
* 100% Stacked Bar Chart 
* 100% Stacked column chart

All 6  charts have same field values:-

* Legend
* Axis
* Value
* color saturation
* Tooltips

when to use bar charts:- when we have compare values across catrgories.

### Line and Area Chart

Power BI has one line chart and two area chart, which are similar to line chart but shaded area under charts.

* line chart
* area chart
* Stacked area  chart

All charts have following fields:-
* Axis
* Legend
* Value
* Tooltip
 when we have to compare value across time best to use line chart.

 ### Combo Chart

 There are two combo charts in Power BI:-
 * Line and stacked column  chart
 * Line and clustered column chart

 Both charts have following fields-
 * shared axis
 * column value
 * colunm  series
 * line value
 * Tooltips

 Combo charts can be appropriate choice when plot two fields that have very different range for instance, dollar amount and percentage.

 ### Ribbon Chart

 Similar to column chart but ribbon chart but it has ribbon between the bars to reflect the changes.
 Charts have four fields-
 * Axis
 * Values
 * legend
 * tooltips

 ### Waterfall chart
 waterfall charts shows the color coded values in running total fashion. By default positive are green and negative values are red.
  The visuals have 4 fields:-
  * Category
  * Breakdown
  * Y-Axis
  * Tooltips
  Waterfall model is good choice when you want to show major changes .

  ### Scatter Chart
   it can be used to visualize two or more metrices for categorical column. Each item  will be plotted on the basis of X and Y coordinates which will be taken fron metrices. if we use third mertric the chart is called bubble chart.
    The cisual have following fields:-
    * Details
    * Legend
    * X-axis
    * Y-axis
    * Size
    * Color Saturation
    * Play Axis
    * Tooltips

### Pie and Doghnuts chart 
 A doughnut chart is similar to a pie chart in that it shows the relationship of parts to a whole.
 The only difference is that the center is blank and allows space for a label or icon.
 Both chart have 4 fields:-
 * Legends
 * Details
 * Values
 * Tooltips
    * Doughnut charts are best used to compare a particular section to the whole, rather than comparing individual sections with each other.

### Tree Map
Treemaps display hierarchical data as a set of nested rectangles.Each level of the hierarchy is represented by a colored rectangle (branch) containing smaller rectangles (leaves).
Power BI bases the size of the space inside each rectangle on the measured value. The rectangles are arranged in size from top left (largest) to bottom right (smallest).
treemap have 5 fields:- 
* Groups
* Details
* Value
* Color saturation
* Tooltips
#### When to use a treemap

Treemaps are a great choice:

* To display large amounts of hierarchical data.

* When a bar chart can't effectively handle the large number of values.

* To show the proportions between each part and the whole.

* To show the pattern of the distribution of the measure across each level of categories in the hierarchy.

* To show attributes using size and color coding.

* To spot patterns, outliers, most-important contributors, and exceptions.

Refference link:- https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-treemaps

### Maps in Power BI

![alt text](.\img\MapInPowerBI.PNG)

Types of map:- map, filled map and shape map

### Funnel

#### When to use a funnel chart

* when the data is sequential and moves through at least 4 stages.
* when the number of "items" in the first stage is expected to be greater than the number in the final stage.
* to calculate potential (revenue/sales/deals/etc.) by stages.
* to calculate and track conversion and retention rates.
* to reveal bottlenecks in a linear process.
* to track a shopping cart workflow.
* to track the progress and success of click-through advertising/marketing campaigns.

#### Working with funnel charts

* Can be sorted.
* Support multiples.
* Can be highlighted and cross-filtered by other visualizations * on the same report page.
* Can be used to highlight and cross-filter other visualizations on the same report page.

Funnel chart have 4 fields:-
* Values
* Group
* color
* tooltips

PowerBI Embedded


![alt text](.\img\Power_BI_Embedded.PNG)




  

