# Deloitte Technology Virtual Experience 
## Analysis of  Daikibo Telemetry Data Using Tableau


### Table of Content

- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tool](#tool)
- [Data Visualization Process](#data-visualization-process)
- [Created Measure](#created-measure)
- [Results](#results)
- [Recommendations](#recommendations)


### Project Overview

 Daikibo Industrials is a heavy machinery manufacturing company with four factories at different locations. The Daikibo tech team aims to understand which locations have the most broken machines and which machine breaks most often. 

 ### Data Source

 Diakibo's Telemetry Data: Deloitte Australia Technology Virtual Experience on Forage. It contains the telemetry data collected from the four factories of the company[Check it out here](https://www.theforage.com/virtual-experience/YPWCiGNTkr6QxcpEu/deloitte-australia/technology-nmwn/coding) 

 ### Tool

 - Tableau: Data Visualization

### Data Visualization Process

1. Upload Daikibo Telemetry Data 
2. Create a calculated measure field "Unhealthy" with the value of 10 for every unhealthy status (representing 10 minutes of potential downtime since the previous message).
3. Create a bar chart: Down Time per Factory.
4. Create a new sheet with a new bar chart: Down Time per Device Type.
5. Create a Dashboard with the 2 previous sheets and set the first chart to be used as a filter

### Created Measure

```tableau
IF[Status]="unhealthy" THEN 10 ELSE 0 END
```

### Results
* Daikibo Factory Seiko has the highest Down Time, with approximately 500 units, indicating significant issues with machinery or operations.
* LaserWelder shows the most Down Time, exceeding 500 units, which indicates it is the most problematic device type across all factories.

### Recommendations 

- For both the LaserWelder and Daikibo Factory Seiko, a detailed analysis should be conducted to identify the underlying causes of downtime.
- Focus on preventive measures for the LaserWelder devices and develop a more robust maintenance plan for Daikibo Factory Seiko.
- Consider training programs for operators on the correct usage and maintenance of the LaserWelders to minimize downtime.
