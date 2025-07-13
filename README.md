<img width="1359" height="197" alt="image" src="https://github.com/user-attachments/assets/60e6788c-1b88-4e80-a22a-0b952bcf39e8" />

## Introduction
Construction360 is a modern data engineering solution designed for the building and infrastructure sector, providing a unified analytics and reporting pipeline tailored to the needs of small-to-mid-sized construction firms. Built on Microsoft Fabric, it empowers stakeholders to consolidate project data from diverse sources into actionable insights.

## Business Use Case
Construction firms often manage multiple projects across different locations, structure types, and teams — leading to data fragmentation and limited visibility into execution trends. Common challenges include missed deadlines, budget overruns, material inefficiencies, and workforce management issues.

Construction360 addresses these challenges by integrating data from operational records, time logs, and procurement documents into a centralized reporting system. Through its Power BI dashboards and Microsoft Fabric-powered pipeline, it enables construction managers to:

- Identify project delays and delivery patterns
- Track material usage to uncover inefficiencies and waste
- Evaluate labor output across sites, tasks, and timelines
- Compare budgeted vs actual costs across locations and structure types


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

## Data Model

<img width="875" height="484" alt="image" src="https://github.com/user-attachments/assets/25c5bce1-ada1-478a-863b-e4caae3b194c" />


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

### Project Summary
![Project Summary](assets/images/Project_Summary.png)
<img width="923" height="528" alt="image" src="https://github.com/user-attachments/assets/4724dc5b-d1c1-406b-a3d3-4ce24e6eddd2" />


### Actual Cost Analysis
![Actual Cost Analysis](assets/images/Actual_Cost_Analysis.png)
<img width="928" height="540" alt="image" src="https://github.com/user-attachments/assets/6f5ee9ed-f0a3-4c14-8fc6-7786e252d356" />
  -100 Projects Analyzed

  -₦252M Budgeted vs ₦442M Actual Spend

  -Locations Covered: Lagos, Abuja, Ondo

  -Delay Rate: 0.75% of projects exceeded schedule
   
## Challenges Faced

- Integrating data from historical records (e.g., scanned PDFs and incomplete Excel sheets)  
- Normalizing material and labor data from different projects with inconsistent units  
- Building a consistent time model for comparing planned vs actual project timelines  
- Limited labeled data for predictive modeling (delay/cost forecasting)  


## Conclusion

This analysis presents key insights from the evaluation of capital projects captured in the construction 360 dataset, comparing planned and actual execution metrics across various dimensions.

A total of ﻿100﻿  projects were analyzed, with a combined budgeted cost of ₦﻿252290885﻿ and an actual spend of ₦﻿442609073﻿. The overall cost variance stands at ₦﻿190318188﻿, indicating whether the portfolio is over or under budget. On average, each project deviated by ﻿1.903.181,88﻿, with ﻿0,75﻿% of all projects exceeding their initial budgets. The project with the highest overrun is ﻿Duplex - Lagos Project 65﻿ , exceeding its budget by ₦﻿11570511﻿.

Geographically, ﻿Lagos﻿ accounts for the highest number of projects with a total actual spend of ₦﻿156168123﻿, suggesting a regional concentration of capital investments. In contrast, ﻿Abuja﻿ had fewer projects.

In terms of efficiency, the average bid duration across all projects is ﻿374,88﻿ days, with ﻿Expansion﻿  taking the longest time to procure and initiate on average. 

Finally, analyzing the unit cost by main work component and UOM reveals that ﻿Landscaping﻿ has the highest cost per unit, while ﻿Road Construction﻿ is the most cost-efficient. These benchmarks are critical for future cost planning and contract evaluation.
