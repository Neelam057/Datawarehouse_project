# Data Warehouse and Analytics Project

## Welcome to the Data Warehouse and Analytics Project repository 🚀

This project demonstrates a **complete end-to-end data warehousing and analytics solution**. It covers everything from building a modern data warehouse to generating actionable insights through SQL analytics.

The project is designed as a **portfolio project** that showcases industry best practices in:

* Data Engineering
* Data Modeling
* ETL Pipeline Development
* SQL Analytics
* Data Architecture

---

# 🏗️ Data Architecture

The project follows the **Medallion Architecture** pattern with three layers:

### 🔷 Architecture Diagram

![Data Architecture](docs/images/data_architecture.png)

### Bronze Layer

* Stores **raw data** as received from source systems. Data is ingested from **CSV files into SQL Server**. No transformations are applied at this stage.

### Silver Layer

* Data is **cleaned, standardized, and normalized**. Data quality issues are resolved. Data is transformed into a structured format for further processing.

### Gold Layer

* Contains **business-ready data models**. Data is organized using a **Star Schema**. Optimized for **analytics and reporting**.

---

# 📖 Project Overview

This project includes the following components:

### Data Architecture

Designing a **modern data warehouse** using **Medallion Architecture** (Bronze, Silver, Gold).

### ETL Pipelines

Building pipelines to **extract, transform, and load data** from source systems into the data warehouse.

### Data Modeling

Creating **fact and dimension tables** optimized for analytical queries.

### Analytics & Reporting

Developing **SQL-based analytics and reports** to derive meaningful business insights.

---

# 🎯 Skills Demonstrated

This repository demonstrates practical experience in:

* SQL Development
* Data Architecture
* Data Engineering
* ETL Pipeline Development
* Data Modeling
* Data Analytics
* Data Warehouse Design

---

# 🛠️ Tools & Technologies

| Tool                                | Purpose                                   |
| ----------------------------------- | ----------------------------------------- |
| SQL Server Express                  | Database for hosting the data warehouse   |
| SQL Server Management Studio (SSMS) | Database management and query tool        |
| GitHub                              | Version control and project collaboration |
| Draw.io                             | Architecture and data modeling diagrams   |
| Notion                              | Project planning and task management      |

---

# 📊 Dataset

The project uses **CSV datasets** from two systems:

* **ERP System**
* **CRM System**

These datasets are loaded into the data warehouse and transformed through multiple layers.

---

# 🚀 Project Requirements

## Building the Data Warehouse (Data Engineering)

### Objective

Develop a **modern SQL Server data warehouse** to consolidate sales data and enable analytical reporting.

### Specifications

**Data Sources**
* Import data from two source systems:
  * ERP
  * CRM
* Data is provided as **CSV files**.
**Data Quality** - Clean and resolve data quality issues before analysis.
**Data Integration** - Combine both sources into a **single analytical data model**.
**Scope** - Focus only on the **latest dataset**. Historical tracking is **not required**.
**Documentation** - Provide clear documentation for Data models, Architecture, Data flows

---

# 📈 BI & Analytics (Data Analysis)

### Objective

Develop **SQL-based analytics** to generate insights into:

* Customer Behavior
* Product Performance
* Sales Trends

These insights help stakeholders understand **key business metrics and trends** for better decision-making.

For detailed requirements, refer to:

```
docs/requirements.md
```

---

# 📂 Repository Structure

```
data-warehouse-project/
│
├── datasets/                           
│   └── Raw datasets from ERP and CRM systems
│
├── docs/                               
│   ├── etl.drawio                # ETL process diagrams
│   ├── data_architecture.drawio  # Data architecture diagram
│   ├── data_catalog.md           # Dataset metadata and field descriptions
│   ├── data_flow.drawio          # Data flow diagrams
│   ├── data_models.drawio        # Star schema data models
│   ├── naming-conventions.md     # Naming standards
│
├── scripts/                            
│   ├── bronze/                    # Raw data ingestion scripts
│   ├── silver/                    # Data cleansing and transformation scripts
│   ├── gold/                      # Analytical data models
│
├── tests/                         
│   └── Data quality and validation scripts
│
├── README.md                      # Project documentation
├── LICENSE                        # License information
├── .gitignore                     # Files ignored by Git
└── requirements.txt               # Project dependencies
```

---

# 📊 Example Business Questions Answered

The analytics layer can answer questions such as:

* Which products generate the highest revenue?
* Which customers contribute the most sales?
* What are the sales trends over time?
* Which regions perform best?

---

# 📜 License

This project is open-source and available under the **MIT License**.

---
