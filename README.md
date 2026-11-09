**🚀 Power BI Galaxy Schema – Data Modeling Portfolio
📌 Project Overview**

This project focuses on designing a structured and efficient data model in Power BI using a Galaxy Schema (Fact Constellation): multiple star schemas that share common (conformed) dimension tables. It covers business requirement analysis, data grain, naming standards, data preparation, fact and dimension tables, relationships, and filter direction.

The objective is to understand how a well-designed data model supports accurate reporting, consistent business metrics, and better report performance across multiple business processes.

**💼 Business Context**

Poor report performance and incorrect numbers are not always caused by dashboard visuals or DAX calculations. The underlying data model can also be a contributing factor.
Issues such as incorrect table relationships, inconsistent granularity, inappropriate filter direction, and poorly structured tables can lead to inaccurate results and inefficient reporting.
This project explores data modeling principles that help address these risks by building a clear, consistent, and maintainable Galaxy Schema.

**🗂️ Model Structure**

**📊 Fact tables (business events and processes)**

fact_sales
fact_order_process
fact_inventory
fact_campaign_spend
fact_promotion_coverage
fact_sales_target

**🧩 Dimension tables (descriptive context)**

dim_date
dim_product
dim_customer
dim_geo
dim_campaign
dim_order_flags

**⚙️ Supporting tables**

_measures – dedicated table that organizes DAX measures
security – supports Row-Level Security (RLS) by region and user email

Each fact table forms its own star with the dimensions around it. Shared dimensions such as dim_date, dim_product, dim_customer, and dim_geo connect several fact tables, which turns the individual stars into a galaxy.

**🛠️ Data Modeling Process**
🔹 Stage 1: Understand the Business and Data
 -Understand the business requirements and reporting objectives.
 -Explore the business processes (sales, order fulfillment, inventory, marketing, targets) and available data.
 -Identify the information required to support reporting and analysis.
 
**🔹 Stage 2: Define the Grain**
 -Establish what each row represents before designing relationships.
 -Define the grain of every fact table clearly.
 -Understand the purpose and level of detail of dimension tables.
 -Avoid connecting tables without understanding their structure and granularity.
 
**✅ Example**:
One row in a customer dimension represents one customer.
One row in a sales fact table represents one sale line, according to the defined business grain.
One row in an inventory fact table represents the units for one product on one date.

**🔹 Stage 3: Establish Naming Standards**
 -Apply consistent naming conventions to tables and columns.
 -Use dim prefixes for dimension tables and fact prefixes for fact tables.
 -Use clear, consistent suffixes such as _key and _id where appropriate.
 -Maintain consistent capitalization and formatting in data values.
 
**🔹 Stage 4: Prepare and Clean the Data**
 -Identify and remove unnecessary columns that do not support reporting requirements.
 -Retain fields needed for analysis, relationships, and business metrics.
 -Use Power Query for data cleaning and transformation, where applicable.
 -Keep the data structure clear and consistent before building the model.
 
**🔹 Stage 5: Build the Galaxy Schema**
 -Organize the model around multiple fact tables and shared dimension tables.
 -Connect dimension tables to fact tables using appropriate keys.
 -Use conformed dimensions (for example, dim_date and dim_product) so that metrics from different fact tables can be analyzed together consistently.
 -Handle role-playing dimensions, such as bill-to and ship-to city on dim_geo, with clearly defined relationships.
 -Avoid unnecessary direct relationships between fact tables.
 -Use an appropriate filter direction, typically from dimensions to facts.
 -Review relationships and granularity to support accurate reporting.
 
**🔹 Stage 6: Organize Measures and Security**
 -Keep all DAX measures in a dedicated _measures table for easier maintenance.
 -Apply Row-Level Security using the security table to restrict data by region and user email.
 
**💡 Key Concepts Covered**
 -Galaxy Schema (Fact Constellation) and Star Schema data modeling
 -Fact tables and dimension tables
 -Conformed and role-playing dimensions
 -Grain and granularity
 -Naming conventions and data standards
 -Data cleaning and transformation
 -Table relationships and key columns
 -Filter direction
 -Measures table and Row-Level Security
 -Model structure, report accuracy, and performance considerations

**🧰 Tools and Technologies**
 -Power BI Desktop – Data modeling and report development
 -Power Query – Data cleaning and transformation
 -Galaxy Schema – Multiple fact tables sharing dimension tables
 -Data Modeling – Relationships, grain, and filter direction
 
**📂 Project Files**

**This repository contains the project materials, which may include:**

Power BI project file (.pbix)
Data modeling notes and documentation
Screenshots illustrating the model and learning process
🎯 Key Learnings
A reliable report starts with a well-designed data model.
Defining the grain before creating relationships helps prevent modeling errors.
Clear naming standards improve model readability and maintainability.
Shared (conformed) dimensions let several business processes be analyzed consistently.
Appropriate relationships and filter direction support more reliable reporting.
When a report is slow or produces unexpected figures, the data model should be investigated alongside visuals and DAX.
📚 Learning Reference

This project was developed as part of my Power BI data modeling learning journey, using the following tutorial as a reference. The tutorial covers Star Schema fundamentals, which this project extends into a multi-fact Galaxy Schema:

**Power BI Star Schema and Data Modeling Tutorial**

👤 Author

Karthik K

This repository documents my practical learning and understanding of Power BI data modeling through Star Schema and Galaxy Schema design.
