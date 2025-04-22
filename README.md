# POWER-BI
**COMPANY**: CODTECH IT SOLUTIONS
**NAME**: Akhila Mangalgi
**INTERN ID**: CT04WT20
**DOMAIN**: POWER BI
**DURATION**: 4 WEEKS
**MENTOR**: NEELA SANTOSH
# DESCRIPTION OF TASK
Task 1:CREATE A SALES DASHBOARD
Data Source and Preparation:
In Power Bi first the datasource choosen was from Excel Workbook,the name of the dataset is Sales_Data.
The Sales_Data consits data of different mobiles sold in different countries,sales,and ratings.
After importing data,i clicked transform data to go into the power query.In Power Query Editor, I performed the following transformations:
Date Handling: Split the Transaction Date into separate columns (Day, Month, Year) and combined them into a standardized Date column .
Data Cleaning: The Day Name column had inconsistencies (e.g., "Sat" vs. "Saturday"). I used Replace Values to standardize entries.
Error Handling: Identified and removed null values in critical columns like Units Sold and Price Per Unit.
Final Steps: Applied Close & Apply to load the cleaned dataset into Power BI.

Visualizations and Dashboard Design:
Now we create visualizations.I have taken few logos from google to place it in the dashboard.I designed an interactive dashboard with the following elements:
Created a slicer containing all months,4 cards which consists of total sales,total quantity,transactions,average added image from the format pane.
A line chart that shows relationship between totalquantity and month,a column chart with totalsales by mobile model,donut chart of transactions by 
payment methods,funnel chart that shows customer ratings,table that shows total sales and total quantity,
a line shart that shows total_sales by day name,map that shows total sales by city and 2 more slicers that show
mobile model and day _name.Aesthetics:Added mobile brand logos (downloaded from Google) for branding.
Customized colors and fonts via the Format Pane for consistency.Created new measures applied dax formulas and created measures:average,total_quantity,
total_sales,transactions.

DAX Measures and Calculations:
Average = AVERAGE(Sales_Data[Price Per Unit])
Total_Quantity = SUM(Sales_Data[Units Sold]) 
Total_Sales = SUMX(Sales_Data,Sales_Data[Units Sold]*Sales_Data[Price Per Unit] )
Transactions = COUNTROWS(Sales_Data) 

For all the visualizations, a common format is what I followed.A visual border with rounded corners(10 px) and a shadow,applied to reamining visualizations using the format painter.
Datalabels and markers are added for clearly knowing what a value is.
Since there were many mobile models,in filter pane in the filtering options TOP N option is choosen and i have choose to place top 3 mobile models in it.

Interactive Filters:
Slicers for Month, Mobile Model, and Day Name allow dynamic data exploration.
This dashboard serves as a centralized decision-making platform, combining raw data processing, advanced analytics, and intuitive visualization to drive measurable business outcomes. 
The architecture supports both real-time monitoring and strategic planning, with all metrics updating dynamically as new data loads.
Raw sales data undergoes Power Query transformation including date standardization, categorical value cleaning, and null value handling. 
The model implements star schema architecture with DAX measures calculating KPIs like total sales (SUMX), month-over-month growth, and average selling price. 
Automated refresh ensures data currency for all visualizations and calculations.
This Power BI dashboard processes sales transaction data through Power Query transformations, implements DAX measures for KPIs, and delivers interactive visualizations including geospatial mapping, temporal trend analysis, and product performance comparisons. 
Features include dynamic filtering, conditional formatting, and drill-through capabilities to support data-driven decision making for sales optimization and inventory management.

Challenges and Solutions :
Issue: The Day Name column had mixed formats.
Fix: Used Replace Values in Power Query.
Issue: Map visual failed to plot cities.
Fix: Manually validated geographic data in Power BI’s Map Settings

Conclusion :
This dashboard provides actionable insights into sales performance, customer preferences, and regional trends. 
The interactive elements (slicers, tooltips) enable users to explore data dynamically.

##OUTPUT


