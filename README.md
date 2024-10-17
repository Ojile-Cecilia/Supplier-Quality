# Supplier-Quality
## Introduction

For manufacturers, maintaining consistent raw material quality is critical to ensuring operational efficiency and reducing costs. However, many companies face challenges with supplier inconsistencies, leading to material defects that disrupt production, cause downtime, and increase expenses.

Managing supplier quality across multiple plants adds complexity. Without a centralized system to track and evaluate supplier performance, manufacturers often lack the visibility needed to identify trends, address performance issues, and improve overall supply chain efficiency. This lack of insight hinders data-driven decision-making, which is essential for enhancing supplier relationships and minimizing production risks.

To address these challenges, a strategic solution is required—one that consolidates supplier data, identifies problem areas, and provides actionable insights. This article explores how business intelligence can be used to optimize supplier quality management, enabling business leaders to make informed, data-driven decisions that positively impact both operations and profitability.

## Problem Statement

Enterprise Manufacturers Ltd. struggled with inconsistent supplier performance monitoring across different plants. The lack of visibility into supplier quality led to frequent production disruptions and inconsistent outputs. In their effort to centralize supplier performance data, management raised several key questions:

- Which vendors/plants are responsible for the highest defect rates?
- Which vendors/plants cause the most downtime?
- Are there specific material-vendor combinations that consistently present issues?
- How does vendor performance vary across different plants?
- Are there overlooked patterns or insights?
- The company needed a clear, data-driven approach to visualize and answer these questions.

Analysis Approach

The core business requirement was clear: “We need to monitor the performance and quality of goods supplied to us.” With no existing procurement system and incomplete data, the goal was to deliver quick insights to improve supplier quality management. The analysis aimed to quantify the financial impact of poor quality and identify the key offenders—vendors, plants, and materials contributing to production inefficiencies.

Rather than presenting stakeholders with abstract metrics like defect counts or downtime minutes, the focus was on highlighting the financial cost of these issues. The goal was to clearly communicate how much money was being lost due to defects and identify the main sources of these problems.

Dataset Overview

The dataset used in the analysis includes the following fields:

Date: When the defect was recorded.
Vendor: The supplier providing the material.
Plant Location: The geographic site of the plant using the material.
Category and Material Type: Classifications of the material.
Defect Type: The nature of the defect.
Total Defect Quantity: The number of defective units recorded.
Total Downtime Minutes: The downtime caused by defective materials.
Methodology

To streamline reporting and improve performance, the data was modeled using a star schema. Key steps included:

Segmenting the dataset into dimension tables based on attributes like Vendor, Plant, and Material Type.
Creating a Fact Table for key metrics like defect quantity and downtime minutes.
Building a Date Table using DAX for time series analysis.
Establishing relationships between the fact and dimension tables to create an efficient star schema data model.
Dashboard Design and Analysis

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






