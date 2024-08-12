# Power BI DEPI

## Session 1: Understanding Key Concepts

### Types of Analysis in Business Intelligence

1. **Descriptive Analytics**:
   - **Objective**: Understand and summarize what has happened in the past.
   - **Example**: Generating monthly sales reports to identify trends.

2. **Diagnostic Analytics**:
   - **Objective**: Explore and analyze why certain events happened.
   - **Example**: Investigating the causes behind a decline in sales.

3. **Predictive Analytics**:
   - **Objective**: Forecast what is likely to happen in the future based on historical data.
   - **Example**: Predicting future sales based on past trends.

4. **Prescriptive Analytics**:
   - **Objective**: Recommend actions to achieve desired outcomes.
   - **Example**: Suggesting marketing strategies to increase sales.

---

### What is ETL?

ETL stands for **Extract, Transform, Load** and is a fundamental process in data integration, particularly within data warehousing and business intelligence. The ETL process is designed to:

1. **Extract**: Gather raw data from various heterogeneous sources such as databases, files, and APIs.
2. **Transform**: Cleanse, format, and apply business rules to the extracted data to ensure consistency and alignment with business objectives.
3. **Load**: Insert the transformed data into a target database, data warehouse, or data lake for further analysis and reporting.

The primary goal of ETL is to ensure that data is accurate, consistent, and readily available for decision-making processes.

#### ETL Process Overview

- **Data Sources**:
  - **Databases**: Structured data from relational (e.g., SQL Server, Oracle) or NoSQL databases (e.g., MongoDB, Cassandra).
  - **Files**: Semi-structured or unstructured data from formats like CSV, JSON, XML.
  - **SaaS Applications**: Data retrieved from cloud-based applications through REST APIs.
  - **Application Events**: Real-time data captured via webhooks or event-driven architecture.

- **Stages of ETL**:
  1. **Extract**:
     - **Objective**: Collect data from various sources with minimal disruption to the source systems.
     - **Challenges**: Managing data heterogeneity, varying formats, and different data velocities.

  2. **Transform**:
     - **Objective**: Convert the extracted data into a format suitable for analysis.
     - **Processes**: Data cleaning, deduplication, normalization, and application of business logic.
     - **Challenges**: Handling inconsistent data, missing values, and maintaining data lineage.

  3. **Load**:
     - **Objective**: Load the transformed data into the final destination, such as a data warehouse or data lake.
     - **Types**: Full load vs. incremental load.
     - **Challenges**: Ensuring data integrity and managing load performance.

- **Supporting Stages**:
  - **Staging Area**:
    - **Role**: Temporary storage for raw data before transformation, allowing for data profiling and validation.
    - **Considerations**: Sizing, performance tuning, and security.

  - **Data Warehouse**:
    - **Role**: Central repository for transformed data, optimized for query performance and data integration.
    - **Considerations**: Schema design (e.g., star, snowflake), indexing, partitioning.

  - **Analytics**:
    - **Role**: Utilizing the data warehouse to derive actionable insights through reports, dashboards, and advanced analytics.
    - **Techniques**: OLAP cubes, data mining, machine learning models.

---

### Q: Is the data model in Power BI a staging area or a data warehouse?

**A**: The data model in Power BI functions more like a **Data Warehouse** rather than a Staging Area.

- **Staging Area**: A temporary holding area where raw data is loaded and transformed. In ETL processes, the staging area is used for intermediate data transformations before loading the data into the final data store. It’s not typically exposed to end-users for analysis.

- **Data Warehouse (Power BI Data Model)**: In Power BI, the data model acts as the final, structured repository of data that has been cleaned, transformed, and optimized for reporting and analysis. This is where relationships between tables are defined, calculated columns and measures are created, and the structure supporting reports and dashboards is set up. The Power BI data model is optimized for efficient querying and analysis, similar to a traditional data warehouse.

Therefore, the **Power BI data model** effectively serves as the **Data Warehouse** in your BI architecture.

---

### What is Power Query?

Power Query is a powerful data connectivity and transformation tool integrated within Microsoft Excel, Power BI, and other Microsoft products. It allows users to:

- Import data from various sources.
- Transform and clean data to create structured datasets.
- Combine and merge data from different sources.

Power Query simplifies the process of preparing data for analysis and reporting, making it an essential tool for business intelligence and data analytics workflows.

---

### Understanding OLAP vs. OLTP and Their Roles in Databases and Data Warehouses

**OLAP (Online Analytical Processing)** and **OLTP (Online Transaction Processing)** are two fundamental data processing systems, each serving different purposes within an organization:

- **OLTP**:
  - **Role**: Typically associated with **databases**.
  - **Purpose**: Manage day-to-day transactional data with a focus on fast, real-time operations.
  - **Optimization**: Designed for handling a large number of short, simple transactions.
  - **Examples**: Banking systems, e-commerce platforms, CRM applications.

- **OLAP**:
  - **Role**: Typically associated with **data warehouses**.
  - **Purpose**: Perform complex analysis and reporting on historical data.
  - **Optimization**: Optimized for read-heavy operations, complex queries, and multidimensional analysis.
  - **Examples**: Business intelligence systems, data marts.

In summary, while OLTP systems and databases are geared toward efficient transaction processing, OLAP systems and data warehouses are designed for in-depth data analysis and decision-making.
