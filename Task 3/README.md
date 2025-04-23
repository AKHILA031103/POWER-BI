TASK 3: REAL-TIME DASHBOARD
## OBJECTIVE:
SET UP A REAL-TIME DASHBOARD USING STREAMING DATA (E.G., FROM AZURE OR A SIMULATED API FEED)
## DESCRIPTION:
## Data Preparation: 
## Sources:
CSV file-sensor_data.csv
- Columns:time,	SensorA,	SensorB	,SensorC
## Power Query Editor:
I took the sensor_data in power bi,now we click on transform data and enter the power query editor.First I started by filtering the number of rows ,filtered the sensors upto value 
less than or equal to 7(<=7) so that i work with data more easily.Next in Sensor A rounded off the value upto 2 decimals,in the Transform ribbon we have an option called rounding there I have
performed these rounding,similarly I have done the same thing for Sencor B and Sensor C.Close and apply the changes.
## Key Visualizations:
Line Charts: That display how each sensor (Sensor1, Sensor2, and Sensor3) performs over time. These visualizations help identify trends, spikes, and gradual changes.The time was filtered out with few values and visualized.
A Clustered Column Chart: is used to compare the maximum values from each sensor, giving a clear picture of which sensor reached the highest recorded measurements.The Maximum value os Sensor A,Sensor B,Sencor C were taken 
on y axis and on X-axis time is taken and few values are filtered out.
Table :which cosinsts of columns time, Sum of Sensor A,Sum of Sensor B,Sum of Sensor C.The time few values are removed and filtered.It provides a raw view of the timestamped data for users who want detailed insights.
Pie Chart:The display of coount of each sensor(Sensor A,Sensor B,Sensor C) in each particular time it was filtered out as above.
KPI:It shows the total sensor count by time which i calculated as a new measure.
Cards:There are 3 cards:Average of Sensor A,Average of Sensor B,Average of Sensor C.
Slicers:I added 4 Slicers :Sensor A,Sensor B,Sensor C,time.
## Formatting:
Added visual border and shadows to all the visualizations.
## Calculation:
TotalSensorCount = SUM(sensor_data[SensorA]) + SUM(sensor_data[SensorB]) + SUM(sensor_data[SensorC])
## Conclusions:
The dashboard simulates a real-time monitoring system by showcasing dynamic charts and visual summaries that could easily be adapted to support streaming or API-fed data sources. 
Although it uses a static dataset, the structure and visualization layout follow a real-world live-data monitoring model — where sensors send continuous updates, and the dashboard reflects the most current state. 
The concept of "live updating" is imitated using refreshable data fields, which could be updated periodically or replaced with incoming data, simulating real-time behavior.
This Power BI dashboard simulates real-time data by using auto-refreshable visuals and dynamic data sources. While it does not connect to an API, it mimics live updates by regularly refreshing the dataset, either manually or via scheduled updates in Power BI Service. As new data replaces the old file, the dashboard adjusts instantly, reflecting current sensor values. 
This approach offers a realistic preview of real-time analytics without requiring complex API integration — ideal for prototyping, testing, or educational purposes.The visuals are structured in a way that, with regular data updates (either manual or scheduled), the dashboard can reflect real-time behavior.
With clean and interactive visuals such as line charts, max value columns, and summary cards, the dashboard effectively communicates key sensor insights. This allows users to quickly interpret trends, compare sensor behaviors, and detect peak values without digging through raw data.
## OUTPUT:







