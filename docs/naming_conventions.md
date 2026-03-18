# Naming Conventions
---
This document outlines the naming conventions used for schemas, tables, views, columns, and other objects in the data warehouse.

## Table of Contents
---
* General Principles
* Table Naming Conventions
  * Bronze Rules
  * Silver Rules
  * Gold Rules
* Column Naming Conventions
  * Surrogate Keys
  * Technical Columns
* Stored Procedures

## General Principles
---
* **Naming Style:** Use `snake_case` (lowercase with underscores `_` to separate words)
* **Avoid Reserved Words:** Do not use SQL reserved keywords as object names

## Table Naming Conventions
---
### Bronze Rules

* All names must start with the **source system name**
* Table names must match their **original names without renaming**

**Format:** <source_system>_<entity>
* `<source_system>`: Name of the source system (e.g., `crm`, `erp`)
* `<entity>`: Exact table name from the source system

**Example:** ```crm_customer_info``` → Customer information from the CRM system

### Silver Rules

* All names must start with the **source system name**
* Table names must match their **original names without renaming**

**Format:** ```<source_system>_<entity>```
* `<source_system>`: Name of the source system (e.g., `crm`, `erp`)
* `<entity>`: Exact table name from the source system

**Example:** ```crm_customer_info```→ Customer information from the CRM system

### Gold Rules

* Use **meaningful, business-aligned names**
* Tables must start with a **category prefix**

**Format:** ```<category>_<entity>``` 
* `<category>`: Role of the table (`dim`, `fact`, `report`)
* `<entity>`: Business-aligned name (e.g., customers, products, sales)

**Examples:** ```dim_customers , fact_sales```

## Glossary of Category Patterns
---
| Pattern | Meaning         | Example(s)                             |
| ------- | --------------- | -------------------------------------- |
| dim_    | Dimension table | dim_customer, dim_product              |
| fact_   | Fact table      | fact_sales                             |
| report_ | Report table    | report_customers, report_sales_monthly |


## Column Naming Conventions
---
### Surrogate Keys

* All primary keys in dimension tables must use the suffix `_key`

**Format:** ```<table_name>_key```
* `<table_name>`: Name of the table/entity
* `_key`: Indicates surrogate key

**Example:** ```customer_key``` → Surrogate key in `dim_customers`

### Technical Columns
---
* All technical columns must start with the prefix `dwh_`

**Format:** ```dwh_<column_name>```
* `dwh`: Indicates system-generated metadata
* `<column_name>`: Describes the column purpose

**Example:** ```dwh_load_date``` → Stores the record load date

## Stored Procedures
---
* All stored procedures for data loading must follow this pattern:
  
**Format:** ```load_<layer>``` * `<layer>`: Target layer (`bronze`, `silver`, `gold`)

**Examples:**

```
load_bronze
load_silver
load_gold
```

