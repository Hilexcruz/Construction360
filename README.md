# Construction360

## Introduction
A modern data engineering for a Building construction shwowing a complete data pipeline and reporting solution for a mid-sized construction company using Microsoft Fabric.

## Business Use Case
Construction360 was built to address the pressing need for unified, real-time analytics in Nigeria’s small-to-mid-sized construction companies. These firms often manage multiple projects with varying structures (e.g., bungalows, flats, modern estates) across cities like Lagos, Ondo, and Abuja, but lack visibility into project delays, budget overruns, material waste, and labor inefficiencies.

Construction360 solves this by delivering a centralized data pipeline and reporting solution using Microsoft Fabric. It enables construction managers to monitor past expererieces:
-Percentage of delayed projects compared to the plan
-Material usage inefficiencies and overuse
-Labor productivity across time and tasks
-Cost variance between budgeted and actual values

## Architecture
1. Ingest data from Sharepoint/OneDrive into Dataflow Gen2
2. Store in OneLake Lakehouse
3. Clean and transform Using Notebooks
4. Create Silver tables with cleaned, joined data
5. Use Power BI semantic model to create:  
  -Project Delay Report
  -Material Effeciency Tracker
  -Location Heat Map
  -Labour Productivity and Progress report
7. Schedule daily refreshes with Pipeline in Fabric
   
## Tools and Stack
1. Microsoft Dataflow Gen2 for ingestion
2. Programming Language - Python (Pyspark)
3. Scripting Language SQL - (TSQL)
4. Pipeline in Data Factory for Orchestration
5. Power Bi for Visualization


## Data Sources
1. Excel
2. Paper Record (PNG)
3. fv\4
4. 4


## Sample Metrics Produced
   
