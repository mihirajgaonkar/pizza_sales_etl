# Near Realtime ETL pipeline using Azure Cloud
![alt text](https://github.com/mihirajgaonkar/pizza_sales_etl/blob/main/diagram.drawio.png?raw=true)
## Overview
This project involves building an ETL (Extract, Transform, Load) pipeline for near-real-time analysis of pizza sales data. The process begins with CSV data stored locally, which is then imported into SQL Server Management Studio (SMSS). An Azure Data Factory (ADF) pipeline, triggered every 15 minutes, moves the data to Azure Blob Storage. Subsequently, the data is mounted into Databricks, where PySpark is utilized to create aggregate tables. The final step involves connecting Databricks with Power BI for visualization.

**Business Questions Answered**:
The ETL pipeline aims to address several key business questions related to pizza sales data:
  Total orders
  Total pizzas sold
  Total revenue
  Pizza sales by month
  Pizza sales by day
  Pizza sales by size
  Pizza sales by category
  Top 5 pizzas

**Databricks Notebook** : [link](https://github.com/mihirajgaonkar/pizza_sales_etl/blob/main/httpsdatabricks-prod-cloudfront.clo.txt) 

![alt text](https://github.com/mihirajgaonkar/pizza_sales_etl/blob/main/dashboard%20ss.png?raw=true)

**Challanges faced**: One challenge encountered during the project was the inability to create a cluster in Azure Databricks due to a quota exceeded issue. This limitation arose from using a free Azure account. To overcome this, the community edition of Azure Databricks was employed as an alternative.
Due to constraints on the free Azure account, it was not feasible to keep the integration runtime and Databricks cluster running continuously. As a workaround, the transformed data was downloaded and loaded into Power BI. Alternatively, you can connect Power BI directly to Databricks for real-time analysis.
