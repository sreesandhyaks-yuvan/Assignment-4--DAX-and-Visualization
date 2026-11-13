# Assignment-4--DAX-and-Visualization
DAX &amp; Data Visualization
Open Power BI Desktop -Select Home - Get data -Text/CSV- List of Orders.csv, Order Details.csv, Sales target.csv
Create a Calculated Column for 'Category Type': Syntax Category Type = 'Order Details (1)'[Category] & " - " & 'Order Details (1)' [Sub-Category]
Calculate Revenue per Order in Order Details Table : Revenue per Order = Revenue = 'Order Details (1)'[Amount] * 'Order Details (1)'[Quantity]
Create measures:- Select Order Details - New measure- Total Sales = SUM('Order Details (1)'[Amount])
Create a Calculated Column to Categorize Sales: Sales Category = Sales Category = IF( 'Order Details (1)'[Amount] >CALCULATE(AVERAGE('Order Details (1)'[Amount]),ALL('Order Details (1)')), "Above Average", "Below Average")
Calculate Order Count: Order Count = DISTINCTCOUNT('Order Details (1)'[Order ID])
Average Profit in Delhi = Create measures:- Select Order Details - New measure. syntax Average Profit in Delhi = CALCULATE(AVERAGE('Order Details (1)'[Profit]),'List of Orders (1)'[State]= "Delhi")
Calculate Year-to-Date (YTD) Sales: Step 1 Calendar = CALENDAR(MIN('List of Orders (1)'[Order Date]), MAX('List of Orders (1)'[Order Date])),step 2 Total Sales = SUM('Order Details (1)'[Amount])
Data Visualization: Sales Target in Clustered column chart. Select the Clustered column chart from the visualization tab of report view. X Axis: Category; Y Axis Total Sales and Sales Target 
Max Profit Margin by Donut chart.  Legend: Sub-Category; Values: Maximum Profit Margin (Syntax: Max Profit Margin = MAX('Order Details (1)'[Profit Margin])) and Profit Margin (Syntax: Profit Margin = DIVIDE('Order Details (1)'[Profit],'Order Details (1)'[Amount])) 
Monthly Sales Trend Line chart X-axis: Order Date (Month/Year); Y-axis:Total Sales
Profit and Quantity by Scatter chart Details: Sub-Category,  X-axis: Quantity; Y-axis: Profit
Comparison of Total Sales Amount and Target: Values: Total Sales; Target 
Sales Performance Matrix: Visualization tab- matrix –  Row- Category, Column- Month, Data field: Sales target and Total Sales. New Measure:- Sales target Syntax Sales Target = SUM('Sales target (1)'[Target])
Geographic Sales Analysis in Map location- Location: List of order(City), Analysis Size/Values: Total Sales
Sales Distribution by Sub-Category in Treemap Group: Sub-Category Values: Total Sales
Order Count by State Funnel chart Category/Group: State; Values: Order Count, Category- list of state
