# 1-	Cleaning Data :
1-Use first row as Header.
2-Remove Blank Rows.
3-Remove Duplicates.
4-Data Type Correction.
# 2-	Data  Muddling :
 -Manage Relation Ship Between the tables   :
 Product_Categories.
 Product_SubCategories.
 Products.
 Sales.
 Customers.
 Calendar.
 Territories.
## 3-DAX :
 -Calculating the Total Quantities Using Sum( ). 
 
 -Calculating the Average Price Using Average ( ). 
 
 -Calculating the Number OF Products Using Count ( ). 
 

# -Calculating the Total Sales =SUMX(Sales,Sales[OrderQuantity]*RELATED(Products[ProductPrice]))

# -Calculating the Total Cost = SUMX(Sales,Sales[OrderQuantity]*RELATED(Products[ProductCost]))

# -Calculating the Profit =[total Sales]-[Total Cost].

# -Calculating the Last Month Order =CALCULATE([TotalOrder],DATEADD('Calendar'[Date],-1,MONTH))

# -Calculating month over month order Duffrins 
Mom Orders Diff = [TotalOrder]-[Last Month Orders]

# -Calculate the change as a percentage 
Mom Orders% Of Change = [Mom Orders Diff]/[Last Month Orders]


#  -Calculate the total orders for the same month last year
Same Month Last Years = CALCULATE([TotalOrder],DATEADD('Calendar'[Date],-1,YEAR))

## 4-Data Visualization (Dashboard ) :
# -Using a slicer to select a time period and display the total quantities and total sales of products during that period in table.
# -  Using KPI to show performance indicators .
-Using the map to show country based on continent selection from the slicer.
-Using Line chart to show total sales for each month .
