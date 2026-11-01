# Power BI Star Schema – Data Modeling Portfolio

## Project Overview

This project focuses on designing a structured and efficient data model in Power BI using the **Star Schema** approach. It covers business requirement analysis, data grain, naming standards, data preparation, fact and dimension tables, relationships, and filter direction.

The objective is to understand how a well-designed data model supports accurate reporting, consistent business metrics, and better report performance.

## Business Context

Poor report performance and incorrect numbers are not always caused by dashboard visuals or DAX calculations. The underlying data model can also be a contributing factor.

Issues such as incorrect table relationships, inconsistent granularity, inappropriate filter direction, and poorly structured tables can lead to inaccurate results and inefficient reporting.

This project explores data modeling principles that help address these risks by building a clear, consistent, and maintainable Star Schema.

## Data Modeling Process

### Stage 1: Understand the Business and Data

- Understand the business requirements and reporting objectives.
- Explore the business process and available data.
- Identify the information required to support reporting and analysis.

### Stage 2: Define the Grain

- Establish what each row represents before designing relationships.
- Define the grain of fact tables clearly.
- Understand the purpose and level of detail of dimension tables.
- Avoid connecting tables without understanding their structure and granularity.

**Example:**
- One row in a customer dimension represents one customer.
- One row in a sales fact table represents one sale, according to the defined business grain.

### Stage 3: Establish Naming Standards

- Apply consistent naming conventions to tables and columns.
- Use `dim` prefixes for dimension tables and `fact` prefixes for fact tables.
- Use clear, consistent suffixes such as `_key` and `_id` where appropriate.
- Maintain consistent capitalization and formatting in data values.

### Stage 4: Prepare and Clean the Data

- Identify and remove unnecessary columns that do not support reporting requirements.
- Retain fields needed for analysis, relationships, and business metrics.
- Use **Power Query** for data cleaning and transformation, where applicable.
- Keep the data structure clear and consistent before building the model.

### Stage 5: Build the Star Schema

- Organize the model around fact and dimension tables.
- Connect dimension tables to fact tables using appropriate keys.
- Avoid unnecessary direct relationships between fact tables.
- Use an appropriate filter direction, typically from dimensions to facts.
- Review relationships and granularity to support accurate reporting.

## Key Concepts Covered

- Star Schema data modeling
- Fact tables and dimension tables
- Grain and granularity
- Naming conventions and data standards
- Data cleaning and transformation
- Table relationships and key columns
- Filter direction
- Model structure, report accuracy, and performance considerations

## Tools and Technologies

- **Power BI Desktop** – Data modeling and report development
- **Power Query** – Data cleaning and transformation
- **Star Schema** – Fact and dimension table design
- **Data Modeling** – Relationships, grain, and filter direction

## Project Files

This repository contains the project materials, which may include:

- Power BI project file (`.pbix`)
- Data modeling notes and documentation
- Screenshots illustrating the model and learning process

## Key Learnings

- A reliable report starts with a well-designed data model.
- Defining the grain before creating relationships helps prevent modeling errors.
- Clear naming standards improve model readability and maintainability.
- Appropriate relationships and filter direction support more reliable reporting.
- When a report is slow or produces unexpected figures, the data model should be investigated alongside visuals and DAX.

## Learning Reference

This project was developed as part of my Power BI data modeling learning journey, using the following tutorial as a reference:

[Power BI Star Schema and Data Modeling Tutorial](https://youtu.be/0A2k62YEbfI?si=LnyJk7Nm6zlQkhje)

## Author

**Karthik K**

This repository documents my practical learning and understanding of Power BI data modeling by Star Schema design.
