# Assignment-4--DAX-and-Visualization
DAX &amp; Data Visualization
Open Power BI Desktop -Select Home - Get data -Text/CSV- List of Orders.csv, Order Details.csv, Sales target.csv
Create a Calculated Column for 'Category Type': Syntax Category Type = 'Order Details (1)'[Category] & " - " & 'Order Details (1)' [Sub-Category]
Calculate Revenue per Order in Order Details Table : Revenue per Order = Revenue = 'Order Details (1)'[Amount] * 'Order Details (1)'[Quantity]
Create measures:- Select Order Details - New measure- Total Sales = SUM('Order Details (1)'[Amount])
Create a Calculated Column to Categorize Sales: Sales Category = Sales Category = IF( 'Order Details (1)'[Amount] >CALCULATE(AVERAGE('Order Details (1)'[Amount]),ALL('Order Details (1)') ), "Above Average", "Below Average")
Calculate Order Count: Order Count = DISTINCTCOUNT('Order Details (1)'[Order ID])
Average Profit in Delhi = Create measures:- Select Order Details - New measure. syntax Average Profit in Delhi = CALCULATE(AVERAGE('Order Details (1)'[Profit]),'List of Orders (1)'[State]= "Delhi")
Calendar = CALENDAR(MIN('List of Orders (1)'[Order Date]), MAX('List of Orders (1)'[Order Date]))
Total Sales = SUM('Order Details (1)'[Amount])
Data Visualization: 
