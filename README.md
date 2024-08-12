# Power BI DEPI

## Session 1

### Types of Analysis

1. **Descriptive Analytics**: Understanding what has happened.
2. **Diagnostic Analytics**: Exploring why events happened.
3. **Predictive Analytics**: Predicting what will happen in the future.
4. **Prescriptive Analytics**: Determining which actions should be taken to achieve a goal or target.

---

### What is ETL?

ETL stands for **Extract, Transform, Load**. It is a cornerstone of data integration, particularly in data warehousing and business intelligence. The ETL process is designed to:

1. **Extract**: Seamlessly gather raw data from various heterogeneous sources.
2. **Transform**: Cleanse, format, and apply business rules to the extracted data to align it with business objectives and ensure consistency.
3. **Load**: Efficiently insert the transformed data into a target database, data warehouse, or data lake for further analysis, visualization, and reporting.

The overarching goal of ETL is to guarantee that data is accurate, consistent, and readily available for decision-making processes.

### ETL Process Overview

#### Data Sources

- **Databases**: Structured data from RDBMS (e.g., SQL Server, Oracle) or NoSQL databases (e.g., MongoDB, Cassandra).
- **Files**: Semi-structured or unstructured data from files such as CSV, JSON, XML.
- **SaaS Applications**: Data obtained from cloud-based applications via REST APIs.
- **Application Events**: Real-time data captured through webhooks or event-driven architecture.

#### Stages of ETL

1. **Extract**:
   - **Objective**: Collect data from various sources, ensuring minimal disruption to the source systems.
   - **Challenges**: Data heterogeneity, varying formats, different data velocities.

2. **Transform**:
   - **Objective**: Convert extracted data into a format suitable for analysis.
   - **Processes**: Data cleaning, deduplication, normalization, applying business logic.
   - **Challenges**: Handling inconsistent data, missing values, and maintaining data lineage.

3. **Load**:
   - **Objective**: Load the transformed data into the final destination (e.g., data warehouse, data lake).
   - **Types**: Full load vs. incremental load.
   - **Challenges**: Ensuring data integrity, managing load performance.

#### Supporting Stages

- **Staging Area**:
  - **Role**: Temporary storage for raw data before transformation, allowing data profiling and validation.
  - **Considerations**: Sizing, performance tuning, and security.

- **Data Warehouse**:
  - **Role**: Central repository for transformed data, optimized for query performance and data integration.
  - **Considerations**: Schema design (star, snowflake), indexing, partitioning.

- **Analytics**:
  - **Role**: Utilizing the data warehouse to derive actionable insights through reports, dashboards, and advanced analytics.
  - **Techniques**: OLAP cubes, data mining, machine learning models.

### Q: Is the data model in Power BI a staging area or a data warehouse?

**A**: The data model in Power BI functions more like a **Data Warehouse** rather than a Staging Area.

- **Staging Area**: This is a temporary holding area where raw data is loaded and transformed. In ETL processes, the staging area is used to perform intermediate data transformations before loading it into the final data store. It’s not typically exposed to end-users for analysis.

- **Data Warehouse (Power BI Data Model)**: In Power BI, the data model serves as the final, structured repository of data that has been cleaned, transformed, and optimized for reporting and analysis. This is where you define relationships between tables, create calculated columns and measures, and set up the structure that supports your reports and dashboards. The Power BI data model is designed for efficient querying and analysis, similar to a traditional data warehouse.

Therefore, the **Power BI data model** is effectively the **Data Warehouse** in your BI architecture.

---

### What is Power Query?

Power Query is a data connectivity and transformation tool that is part of Microsoft Excel and other Microsoft products. It allows users to import, transform, and manipulate data from various sources to create clean, structured datasets for analysis and reporting. Power Query simplifies the process of cleaning, shaping, and merging data from different sources, making it a powerful tool for data preparation and analysis in business intelligence and data analytics workflows.

![Screenshot 2024-08-12 224331](https://github.com/user-attachments/assets/effe90f3-6d9f-4b08-8db7-957d9e182ee0)


### Summary: Understanding OLAP vs. OLTP and Their Roles in Databases and Data Warehouses

OLAP (Online Analytical Processing) and OLTP (Online Transaction Processing) are two fundamental data processing systems that serve different purposes within an organization.

- **OLTP** is typically associated with **databases**. These systems are designed for managing day-to-day transactional data, focusing on fast, real-time operations. OLTP databases are optimized for handling a large number of short, simple transactions, such as those found in banking systems, e-commerce platforms, and CRM applications.

- **OLAP** is typically associated with **data warehouses**. These systems are used for complex analysis and reporting on historical data, focusing on read-heavy operations. OLAP data warehouses are optimized for performing complex queries, aggregations, and multidimensional analysis, making them essential for business intelligence and analytics applications.

In summary, while OLTP systems and databases are geared toward efficient transaction processing, OLAP systems and data warehouses are designed for in-depth data analysis and decision-making.
