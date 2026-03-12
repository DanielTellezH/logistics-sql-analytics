logistics-analytics-sql-project

This project analyzes logistics operations to identify factors affecting delivery delays, route efficiency, and vehicle performance.
The analysis combines Python, SQL, and Power BI to transform raw shipment data into operational insights.

Business Problem

Logistics operations often experience delays that impact service reliability and operational efficiency. This project aims to answer key operational questions:

Which routes generate the highest delays? Which vehicles have lower performance? What operational factors contribute to delivery delays?

Data Pipeline

Raw Dataset ↓ Python Data Cleaning ↓ SQL Analysis ↓ Power BI Dashboard

Data Processing

Data preparation was performed using Python.

Key steps included:

Handling missing values
Removing duplicate records
Calculating delivery delays
Feature engineering Example:
df["delay_minutes"] = ( df["actual_delivery"] - df["scheduled_delivery"] ).dt.total_seconds() / 60

SQL Analysis

SQL queries were used to analyze operational metrics. Example query:

SELECT route, AVG(delay_minutes) AS avg_delay, COUNT(*) AS shipments FROM shipments GROUP BY route ORDER BY avg_delay DESC;

Additional analyses included:

Route performance
Vehicle efficiency
Delay distribution
Operational trends
Dashboard

The Power BI dashboard provides an overview of logistics performance, including:

Operational KPIs
Route performance
Vehicle analysis
Delay trends
Key Insights

Example findings:

22% of delays occur in only 3 routes.
Heavy shipments increase average delay by 18%.
Certain vehicles show consistently lower performance.
Recommendations

Based on the analysis:

Review routes with highest delays
Redistribute heavy shipments across time windows
Evaluate performance of underperforming vehicles