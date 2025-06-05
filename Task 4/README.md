Task 4:INTEGRATION WITH PYTHON OR R
## OBJECTIVE:
USE PYTHON OR R SCRIPTS WITHIN POWER BI TO PERFORM ADVANCED DATA ANALYSIS OR VISUALIZATIONS.
## DESCRIPTION:
## DATA PREPARATION:
CSV File(sales_data_sample.csv)
- COLUMNS:ORDERNUMBER,QUANTITYORDERED,PRICEEACH,ORDERLINENUMBER,SALES,ORDERDATE,STATUS,QTR_ID,
MONTH_ID,YEAR_ID,PRODUCTLINE,MSRP,PRODUCTCODE,CUSTOMERNAME,PHONE,ADDRESSLINE1,ADDRESSLINE2,
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
-> Boxplot by City:
To create a boxplot showing Sales by City,I used the following code in the R script editor:
library(ggpubr)

ggpubr::ggboxplot(dataset, 
                  x = "CITY",          
                  y = "SALES",
                  color = "CITY",      
                  fill = "pink",       
                  width = 0.3)
                  
-> Grouped Boxplot by Deal Size, City, Product Line, Sales:
To create a grouped boxplot place DEALSIZE,CITY,PRODUCTLINE,SALES in values after that in r script editor:
library(ggplot2)
library(ggpubr)
ggpubr::ggboxplot(dataset,
          x = "DEALSIZE",
          y = "SALES",
          color = "PRODUCTLINE",
          facet.by = "CITY",
          palette = "npg",
          short.panel.labs = TRUE)

-> Histogram by sales:
To create a histogram showing Sales ,I used the following code in the R script editor:
library(ggplot2)
library(ggpubr)
gghistogram(dataset,"SALES",bins=15,fill="lightgreen",border="black")

->Grouped Histogram by Quantityordered,State,Dealsize:
To create a grouped histogram place QUANTITYORDERED,STATE, DEALSIZE in values after that in r script editor I wrote the following code:
library(ggplot2)
library(ggpubr)
gghistogram(
  data = dataset,                   
  x = "QUANTITYORDERED",            
  facet.by = c("STATE", "DEALSIZE"),
  bins = 15,                        
  color = "STATE",                  
  fill = "STATE",                   
  palette = "jco",                  
  ggtheme = theme_pubr()            
)

->Scatter Plot by Productline,Priceeach,Sales,Quantityordered:
To create a scatter plot place PRODUCTLINE,PRICEEACH,SALES,QUANTITYORDERED in values then in r script editor:
library(ggplot2)
library(ggpubr)
ggscatter(dataset, 
          x="QUANTITYORDERED", 
          y="PRICEEACH",
          color="PRODUCTLINE",
          size="SALES",
          alpha=0.3
        )

-> Q-Q Plot by MSRP:
To create a q-q plot place MSRP in values then in r script editor I wrote the following code:
library(ggplot2)
library(ggpubr)
ggqqplot(dataset,"MSRP",conf.int.level=0.95,color="navy")

->Slicers:3 slicers which include CITY,STATUS,DEALSIZE.
->Cards:Max of SALES,Count of QUANTITYORDERED,Average of MSRP.

## Conclusion:
The sales dashboard provides valuable insights into performance across cities, deal sizes, product lines, and customer behavior. From the boxplot, we see that North Sydney has higher variability in sales, while Melbourne maintains more consistent performance. Sales are strongest in the Classic Cars and Motorcycles product lines, particularly in the Medium and Small deal sizes. The histogram shows that most sales transactions fall below 5,000, indicating a concentration of lower-value deals. Quantity ordered varies by state and deal size, with NSW exhibiting higher activity across all deal sizes than Victoria. The Price Sensitivity Analysis scatter plot suggests no strong linear correlation between quantity ordered and price, indicating diverse customer preferences. Lastly, the Q-Q plot for MSRP shows data is reasonably normally distributed, confirming its suitability for predictive modeling.

## OUTPUT:
![Image](https://github.com/user-attachments/assets/6e03eddd-0089-4e56-af7e-51b444f10842)



