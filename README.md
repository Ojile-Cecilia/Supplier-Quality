# Improving Supplier Quality Management Through Business Intelligence: A Strategic Approach for Manufacturers

## Introduction

For manufacturers, maintaining consistent raw material quality is critical to ensuring operational efficiency and reducing costs. However, many companies face challenges with supplier inconsistencies, leading to material defects that disrupt production, cause downtime, and increase expenses.

Managing supplier quality across multiple plants adds complexity. Without a centralized system to track and evaluate supplier performance, manufacturers often lack the visibility needed to identify trends, address performance issues, and improve overall supply chain efficiency. This lack of insight hinders data-driven decision-making, which is essential for enhancing supplier relationships and minimizing production risks.

To address these challenges, a strategic solution is required—one that consolidates supplier data, identifies problem areas, and provides actionable insights. This article explores how business intelligence can be used to optimize supplier quality management, enabling business leaders to make informed, data-driven decisions that positively impact both operations and profitability.

## Problem Statement

Enterprise Manufacturers Ltd. struggled with inconsistent supplier performance monitoring across different plants. The lack of visibility into supplier quality led to frequent production disruptions and inconsistent outputs. In their effort to centralize supplier performance data, management raised several key questions:

1. Which vendors/plants are responsible for the highest defect rates?
2. Which vendors/plants cause the most downtime? 
3. Are there specific material-vendor combinations that consistently present issues?
4. How does vendor performance vary across different plants?
5. Are there overlooked patterns or insights?
6. The company needed a clear, data-driven approach to visualize and answer these questions.

## Analysis Approach

The core business requirement was clear: 

*“Our company wants to start monitoring the performance and quality of goods sent to us. We don’t have a procurement system in place, and while we lack complete data, we need insights to monitor and improve this activity quickly.”*

With no existing procurement system and incomplete data, the goal was to deliver quick insights to improve supplier quality management. The analysis aimed to quantify the financial impact of poor quality and identify the key offenders—vendors, plants, and materials contributing to production inefficiencies.

Rather than presenting stakeholders with abstract metrics like defect counts or downtime minutes, the focus was on highlighting the financial cost of these issues. The goal was to clearly communicate how much money was being lost due to defects and identify the main sources of these problems.

## About the Dataset
The dataset used in the analysis includes the following fields:

- **Date:** When the defect was recorded.
- **Vendor:** The supplier providing the material.
- **Plant Location:** The geographic site of the plant using the material.
- **Category and Material Type:** Classifications of the material.
- **Defect Type:** The nature of the defect.
- **Total Defect Quantity:** The number of defective units recorded.
- **Total Downtime Minutes:** The downtime caused by defective materials.
  
## Methodology

To streamline reporting and improve performance, the data was modeled using a star schema. Key steps included:

## Segmenting the dataset into dimension tables: After analyzing the data, I identified attributes that could be divided into separate dimension tables. 
By breaking the data into smaller, manageable parts, I created dimension tables with unique identifiers for categories such as **Vendor, Plant Location, Material Type,** and **Defect Type**.


The objective was to develop a model optimized for efficient querying and insightful reporting. Here’s an overview of the steps I took:  

- **Duplicate the Query**: For each required dimension table, I duplicated the original query.
     
- **Rename the Tables**: Each query was renamed based on its role in the model, such as the Supplier Fact Table for central metrics like defect quantity and downtime minutes, and Dimension Tables for categories like **Vendor,** **Plant Location, Defect, Defect Type, Category,** and **Material Type.**

- **Select Relevant Columns**: For each table, I retained only the columns specific to that dimension. This step streamlined the dataset, ensuring each table contained only the essential information for analysis. Additionally, I created primary keys for each dimension by generating an index column.  

- **Building the Fact Table**: After establishing the dimension tables, I used Power BI's Merge feature to incorporate the keys back into the original dataset, resulting in a well-structured Fact Table.

**Creating a Date Table**: A crucial step in the process was building a dedicated Date Table. In data analysis, a Date Table is essential for creating time intelligence measures and applying time-related filters to reports. Using DAX (Data Analysis Expressions), I created an accurate Date Table that facilitated effective time series analysis, enabling the tracking of trends over time.

**Star Schema Data Model**: With the Dimension and Fact Tables prepared, the next step was to design the data model. I established relationships by linking the primary keys in the dimension tables to the foreign keys in the Fact Table. This resulted in a streamlined Star Schema Model. Organizing the data in this manner ensures efficient report generation without performance issues.

## **Analysis**:  
With the data prepared, the next challenge was designing a dashboard that provided actionable insights at a glance. I aimed to strike a balance between high-level summaries for executives and detailed breakdowns for procurement and production teams.  

The primary challenge was defining the right metrics based on the available data. I focused on three key metrics:  

- **Downtime**: Total hours lost due to defective materials.  
- **Defect Quantity**: The number of defective units received from suppliers.  
- **Downtime Cost**: The financial impact, assuming a loss of $10 for every hour of downtime.  

Initially, I questioned whether including defect quantity added value since there was no direct comparative data. However, I realized that there might be a potential correlation between downtime and defects, which proved correct. For example, some instances showed fewer defects but higher downtimes and vice versa.  

I also needed to determine whether to present downtime in minutes or hours. I opted for hours to align with the manufacturing industry’s standard of calculating costs on an hourly basis, ensuring consistency.  

Another question that arose was why downtime persisted even when defects seemed unrelated. I hypothesized that other factors, such as machine failures, power outages, staffing shortages, or delays in receiving materials, could contribute to the issue.


The homepage was designed to deliver a clean and professional interface with intuitive navigation tailored for stakeholders. A navigation bar was incorporated to allow users to seamlessly switch between the main sections of the report, each highlighting different aspects of supplier quality and performance. The layout takes inspiration from modern website designs, ensuring even non-technical decision-makers can easily access essential metrics.  

The emphasis was on utilizing graphic design to craft a visually appealing and user-friendly dashboard, making it simple for stakeholders to locate critical metrics at a glance.



The final dashboard provided high-level summaries for executives and detailed breakdowns for procurement and production teams. Key metrics included:

Downtime: Total hours lost due to defective materials.
Defect Quantity: The number of defective units from suppliers.
Downtime Cost: Financial losses due to downtime (assumed at $10/hour).
Insights included:

A rising trend in defects and downtime, leading to significant financial losses.
Identification of the worst-performing vendors and plants.
Analysis of vendor-material and vendor-plant combinations to identify the most problematic relationships.
Key Insights and Recommendations

Rising Defects and Downtime: Defects surged to 2.6 billion units, with 216,000 hours of downtime, resulting in $2.16 million in financial losses.
Worst-Performing Vendors: Certain suppliers were identified as high-risk, requiring targeted improvement initiatives.
Plant-Specific Issues: Several plants were highlighted as significant contributors to defect-related downtime.
Material Performance: Raw materials were the most problematic, with a need for process and supply chain improvements.
Recommendations:

Centralize Data and Automate Reporting: Implement a centralized system to track and evaluate supplier performance across all plants.
Focus on Financial Impact: Emphasize the financial costs of supplier quality issues to drive data-driven decision-making.
Implement a Continuous Improvement Program: Establish programs to reduce downtime, improve material quality, and hold suppliers accountable.
Leverage Advanced Analytics: Use predictive models to address issues before they result in significant downtime or material waste.
Conclusion

Business intelligence tools can transform supplier quality management by turning raw data into actionable insights. For Enterprise Manufacturers Ltd., this BI-driven approach revealed trends and inefficiencies that were previously unnoticed. Centralizing procurement and performance data through Power BI will allow for more informed decision-making, improving supplier relationships and operational efficiency in the long term.






