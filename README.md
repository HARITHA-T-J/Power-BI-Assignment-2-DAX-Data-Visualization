# Power-BI-Assignment-2-DAX-Data-Visualization
E-Commerce Sales Analysis
●	Created a Calculated Column for 'Category Type':Add a calculated column in the Order Details table that combines the 'Category' and 'Sub-Category' columns into a single 'Category Type' column-select order details table-Go to table tools-new column-and using this syntax for creating a new column named Category Type Category_Type = 'Order Details (1)'[Category]& " - " &'Order Details (1)'[Sub-Category]
●	CalculatedRevenue per Order in Order Details Table:Create a calculated column in the Order Details table to compute the revenue (Amount * Quantity) per order-select order details table-Go to table tools-new column-and using this syntax for creating a new column named Revenue = 'Order Details (1)'[Amount]*'Order Details (1)'[Quantity]
●	Created a Calculated Column to Categorize Sales: Add a calculated column named ‘Sales Category’ in the Order Details table that categorizes each order as 'Above Average' or 'Below Average' based on the Amount value.select order details table - go to table tools-add new column named Sales category using this syntax Sales Category = if('Order Details (1)'[Amount]>AVERAGE('Order Details (1)'[Amount]),"Above Average","Below Average")
Calculated Measures:
●	Calculated Order Count: Define a measured to count the total number of orders in the Order Details table.select order details table-go to table tools-select new measure then use this syntax Order Count = COUNT('Order Details'[Order ID]) then go to-report view-then select a card then select value-order count then the card shows the total oder counts -560
●	Calculated Average Profit in Delhi: Created a measure to calculate the average profit for orders placed in Delhi.select the order details table-go to tools-new measure then using this syntax -Avg Profit in Delhi = CALCULATE(AVERAGE ('Order Details (1)'[Profit]),'List of Orders (1)'[City] = "Delhi") to view go to report view then select a card and give value avg profit in delhi and it is 15.97.
●	Calculate Year-to-Date (YTD) Sales: Define a measure to calculate the total sales amount accumulated from the earliest order date up to each order date-select the order details table-go to table tools-new measure- using this syntax, YTD Sales = TOTALYTD(SUM('Order Details (1)'[Amount]),'List of Orders (1)'[Order Date]) then go ro report view add a card and give a value such as ytd sales it will be 432 k.
Data Visualization:
Sales Target Achievement by Category: Compare actual sales with sales targets by category using a clustered column chart.go to report view add a new page named sales target v/s catgeory then select a clustered column char from from build visual then add values like category and sales target in x and y axis then format visuals.
Max Profit Margin by Sub-Category: Analyze the maximum profit margin for each sub-category of products using a donut chart-Go to report view-add a new page named profit margin and sub category then select build visual-select Doughnut chart-then add values appropriately -using format visuals for best result.
Monthly Sales Trend: Show the trend of monthly sales over time using a line chart-go to report view-build visual-line chart- then add values like month and month appropriately in both y and x axis make format page to make best result.
Comparison of Profit and Quantity by Sub-Category: the relationship between profit and quantity sold for different sub-categories using a scatter chart.go to report view-build visual-select scatter plot chart-add sub category,x axis as sum of qty and y axis as sum of profit,legend as sub category and siza as count of sub category.
Comparison of Total Sales Amount and Target: Create cards to succinctly display the total sales amount alongside the sales target for quick comparison and analysis. Also, create a multi-row card Compare to display the minimum target for each segment-go to report view-add a card and add value as sum of amount  and give title as total sales and add a card add value as sum of target give title as total sales target .then add a card and add value as total sales target and title named minimum target by segment add category as value.select drop down value of total sales target select minimum.use format visuals for appropriate changes.
Sales Performance Matrix: Build a matrix view to analyze how actual sales compare to sales targets across different categories and months-go to report view-build visual-add a matrix then add row as category,coloumns as month and value as sum of target.
Geographic Sales Analysis: Visualize total sales on a map by city to identify regional sales patterns-go to report view-build visuals-select map -add location as city- bubble siza as sum of amount.go to report view-build visuals -select tree map give category as sub category,details as category and value as sum of amount.
Order Count Analysis by State: Create a funnel chart to visualize the distribution of order counts across different states-go to report view-select funnel chart from build visual-then add category as state and value as order count.








