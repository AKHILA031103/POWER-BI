Task 2:DATA INTEGRATION FROM MULTIPLE SOURCES
# Objective:
COMBINE DATA FROM AT LEAST TWO DIFFERENT SOURCES (E.G., EXCEL AND SQL SERVER) TO CREATE A UNIFIED REPORT.
# Description of task:

Data import and cleaning:
I have taken data from two different sources ,one is excel workbook the data is Books_Data_Clean and another is a text/csv file named as book_dataset.
The dataset book_dataset was clean soI loaded it,next i went to get data and clicked on excel workbook choose the Book_Data_Clean and transformed it.Entered the power
query editor,checked for  errors,there were no errors so i closed and applied it.
The Book_Data_Clean consits:index,Publishing Year	,Book Name,Author,language_code,	Author_Rating	,Book_average_rating,	Book_ratings_count,
genre,	gross sale,s	publisher revenue	,sale price,	sales rank,	Publisher 	,units sold.
The book_dataset consists of:Author,BookID,Genre,Rating,Title,Year.

Data Model View:
Go to model view in Power Bi,next I have 2 different datasets, so i had to make a relationship between them to visualize them.
Books_Data_Clean[Author]->book_dataset[Author]
Books_Data_Clean[Book Name]->book_dataset[Title]
Books_Data_Clean[Publishing Year]->book_dataset[Year]
These one to one relationships helps in building the models and visualizations.

Creating Dashboard:
A clustered column chart with x axis as:Author and y axis as :Average,here  the number of authors were filtered top 10 authors by
average of book rating,turned on the data labels added bacground and visual border with rounded squares.
A pie chart with book count by genre added datalabels,legend,colors to different genres,visual border with rounded corners.
A funnel chart with sum of bookID by author ,with datalabels,visual boder and background,rounded corners.
A line chart with x axis as: year and y axis as: average of rating ,added datalabeles,changed the line chart style to dotted line chart,
added datalabels,background to datalabels,visual border,rounded rectangles,markers.
A gauge chart with value as sum of unit sold,minimum value as min of units sold maximum value was calculated and target value was calculated.
Line and clustered column chart with -axis as Publishing year ,column y-axis as sum of gross sales,line y-axis as sum of book average rating,
legends are added on top left ,border,background,rounded circles were added.Publishing year top 5 by average of gross sales were considered and i have done it in filter pane.
KPI with value as sum of units sold,trend axis as publishing year,target as target sales.
A table with 2 columns showing publisher,sum of publisher revenue.The publisher was filtered out as top 5 by sum of publisher revenue and in table total is added.
Added different colors as background ,bold the value of total.
A waterfall chart with category as publisher,y axis as sum of gross sales,the positive value are shown with green and negative as blue.
3 Slicers :Author of one dataset,author of another dataset,rating.

Measures:
MaxSales = 1000000
TargetSales = 90000

Conclusions:
This Power BI dashboard presents a comprehensive overview of book sales and ratings across different dimensions. It includes a variety of visualizations to analyze data from multiple perspectives.
At the top, there are slicers to filter data by Author and Rating, allowing for interactive data exploration.
In Book Ratings by Author ,Frances Hodgson Burnett and Nora Roberts appear to have received the highest average ratings, indicating strong reader satisfaction.
In Sum of BookID by Author,Dan Brown standing out for contributing the highest number of entries.
In Sales vs Ratings Over Years ,it suggests how both commercial success and reader ratings have trended since the 1600s, offering insights into historical patterns.
In Average Rating by Year ,the fluctuations in reader ratings over the decades. Notable peaks occur in the 1960s and 1980s, followed by a dip in the 2000s.
In Book Count by Genre , Fantasy is the dominant genre, making up 40%, followed by Classic, Dystopian, and Thriller—each accounting for 20%.
In Yearly Sales Performance, This KPI card highlights the total sales figure of 91,276 units, slightly exceeding the target of 90,000, a 1.42% increase.
In Sales Performance Indicator ,It tracks progress towards a 10M sales benchmark, emphasizing the current standing in a visually intuitive manner.
In Sales Contribution & Publisher Revenue, A stacked column chart shows how different publishers contribute to overall sales. A table ranks publishers by revenue, with Amazon Digital Services, Inc. as the top earner, contributing over 1.48 million.
Overall, this dashboard integrates both qualitative and quantitative data for a 360-degree view of the publishing landscape—ideal for strategic planning, marketing, and editorial decisions.

# OUTPUT:
![Image](https://github.com/user-attachments/assets/c60f47db-2758-4541-84c2-cb71afd55440)

