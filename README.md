# Construction360

## Introduction
A modern data engineering for a Building construction shwowing a complete data pipeline and reporting solution for a mid-sized construction company using Microsoft Fabric.

## Business Use Case
Construction360 was built to address the pressing need for unified, real-time analytics in Nigeria’s small-to-mid-sized construction companies. These firms often manage multiple projects with varying structures (e.g., bungalows, flats, modern estates) across cities like Lagos, Ondo, and Abuja, but lack visibility into project delays, budget overruns, material waste, and labor inefficiencies.

Construction360 solves this by delivering a centralized data pipeline and reporting solution using Microsoft Fabric.  
It enables construction managers to monitor past experiences:

- Percentage of delayed projects compared to the plan  
- Material usage inefficiencies and overuse  
- Labor productivity across time and tasks  
- Cost variance between budgeted and actual values


## Architecture
<img width="1415" height="725" alt="Screenshot 2025-07-10 145122" src="https://github.com/user-attachments/assets/2ad372cc-b53d-46c9-9f63-8dbbf2d0387b" />

1. Ingest data from SharePoint/OneDrive into Dataflow Gen2  
2. Store in OneLake Lakehouse  
3. Clean and transform using Notebooks  
4. Create Silver tables with cleaned, joined data  
5. Use Power BI semantic model to create:  
    - Project Delay Report  
    - Material Efficiency Tracker  
    - Location Heat Map  
    - Labour Productivity and Progress Report  
6. Schedule daily refreshes with Pipeline in Fabric

## Tools and Stack
1. Microsoft Dataflow Gen2 for ingestion
2. Programming Language - Python (Pyspark)
3. Scripting Language SQL - (TSQL)
4. Pipeline in Data Factory for Orchestration
5. Power Bi for Visualization


## Data Sources
1. Excel
2. Paper Record (PNG)
3. Time tracking logs (CSV)
4. Site Photos
   
## Sample Metrics Produced
   
## Challenges Faced

- Integrating data from historical records (e.g., scanned PDFs and incomplete Excel sheets)  
- Normalizing material and labor data from different projects with inconsistent units  
- Building a consistent time model for comparing planned vs actual project timelines  
- Limited labeled data for predictive modeling (delay/cost forecasting)  


## Conclusion

Construction360 demonstrates how Microsoft Fabric can be used to solve real-world infrastructure and project visibility problems in the construction sector.  
By automating data ingestion, transformation, and reporting, this solution empowers construction managers to make faster, data-driven decisions and better manage timelines, costs, and labor efficiency.  
Future versions of this project may include predictive analytics and geospatial site progress tracking.
