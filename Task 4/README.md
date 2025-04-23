Task 4:INTEGRATION WITH PYTHON OR R
## OBJECTIVE:
USE PYTHON OR R SCRIPTS WITHIN POWER BI TO PERFORM ADVANCED DATA ANALYSIS OR VISUALIZATIONS.
## DESCRIPTION:
## DATA PREPARATION:
CSV File(sales_data_sample.csv)
-COLUMNS:ORDERNUMBER,QUANTITYORDERED,PRICEEACH,ORDERLINENUMBER,SALES,ORDERDATE,STATUS,QTR_ID,MONTH_ID,YEAR_ID,PRODUCTLINE,MSRP,PRODUCTCODE,CUSTOMERNAME,PHONE,ADDRESSLINE1,ADDRESSLINE2,
CITY,STATE,POSTALCODE,COUNTRY,TERRITORY	,CONTACTLASTNAME,CONTACTFIRSTNAME,DEALSIZE.
## POWER QUERY EDITOR:
I have taken the sales_data_sample dataset and transform data ,we enter into power query editor I filtered the rows which were empty ,editied the city column.Close and apply 
the changes now the data is loaded.
## Key Visualization:
Boxplot:x axis as city , y axis as sales.
Bar Chart:Sales by count.
Scatter plot:x axis as quantityordered and y axis as priceeach.
Q-Q Plot : MSRP
Slicers:City,Status,Dealsize.
Cards:Max of Sales,Count of Quantityordered,Average of MSRP.
## RStudio:
I opened Rstudio,and in the console installed few packages
install.pacakges("ggplot2")
library(ggplot2)
install.packages("ggpubr")
library(ggpubr)
## Key Visualizations:
Now in Power Bi open the visaulization pane and select RScript visual,it will open an R script editor:
To create a Boxplot:place the SALES,CITY in the values after doing that i wrote a r-program:
library(ggplot2)
library(ggpubr)

ggpubr::ggboxplot(dataset, 
                  x = "CITY",          
                  y = "SALES",
                  color = "CITY",      
                  fill = "pink",       
                  width = 0.3)
To create a grouped boxplot:place DEALSIZE
