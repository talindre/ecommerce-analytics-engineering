# Analytics Engineering Roadmap

## Project Goal

Build a complete Analytics Engineering portfolio project that demonstrates:

- SQL proficiency
- Data modeling
- Data warehouse thinking
- Snowflake fundamentals
- dbt transformations
- Git and GitHub workflows
- Business intelligence reporting with Power BI
- Documentation and professional project structure

Target completion: January

---

# Success Criteria

By January I should have:

- A professional GitHub repository
- A complete end-to-end analytics project
- Strong SQL foundations
- Basic dimensional modeling skills
- Snowflake experience
- A functioning dbt project
- Power BI dashboard(s)
- Professional documentation
- Consistent Git commit history

---

# Technology Stack

## Core Stack (Before January)

### SQL
Primary skill.

Topics:

- SELECT
- WHERE
- ORDER BY
- Aggregations
- GROUP BY
- CASE WHEN
- JOINS
- CTEs
- Subqueries
- Date Functions
- Window Functions
- Business Analysis Queries

---

### Data Modeling

Topics:

- Fact Tables
- Dimension Tables
- Star Schema
- Data Grain
- Business Metrics
- Customer Analytics
- Product Analytics

---

### Snowflake

Topics:

- Databases
- Schemas
- Warehouses
- Data Loading
- Raw Layer
- Staging Layer
- Analytics Layer

---

### dbt

Topics:

- Sources
- Models
- Testing
- Documentation
- Staging Models
- Fact Models
- Dimension Models

---

### Git & GitHub

Topics:

- Cloning
- Branching
- Commits
- Pulling
- Pushing
- Documentation

---

### Power BI

Topics:

- Data Modeling
- KPI Design
- Executive Dashboards
- Business Metrics

---

# Deferred Until After January

- Dagster
- Prefect
- Airflow
- AWS
- Azure
- Databricks
- Spark
- Great Expectations
- Elementary
- Advanced Python
- Machine Learning
- Deep Learning

---

# Project Overview

Dataset:

Olist Brazilian E-Commerce Dataset

Project Name:

Ecommerce Analytics Engineering Project

Business Objective:

Transform raw ecommerce data into business-ready reporting assets using modern analytics engineering practices.

---

# Planned Architecture

Raw CSV Files
↓
SQL Exploration
↓
Dimensional Modeling
↓
Snowflake
↓
dbt
↓
Analytics Models
↓
Power BI Dashboards

---

# Repository Structure

```text
ecommerce-analytics-engineering/

├── README.md
├── career-log.md
│
├── docs/
│   ├── business_questions.md
│   ├── data_dictionary.md
│   ├── architecture_notes.md
│   └── project_roadmap.md
│
├── sql/
│   ├── exploration/
│   └── analysis/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── diagrams/
│
├── screenshots/
│
└── .gitignore
```

---

# Professional Habits

Every session:

1. Pull latest changes
2. Work
3. Commit work
4. Push work
5. Update career log

---

# Commit Message Examples

Good:

- Initial project structure
- Added customer exploration analysis
- Documented Olist tables
- Added revenue trend queries
- Designed star schema
- Added dbt staging models

Avoid:

- update
- stuff
- test
- fix

---

# Six Week Plan

---

# Week 1

Goal:

Understand the business and dataset.

Deliverables:

- Repository setup
- Data dictionary
- Initial business understanding

Topics:

- SQL Refresh
- Data Exploration
- Business Context

---

## Day 1

Setup and Dataset Exploration

Tasks:

- Setup repository (Complete)
- Setup structure (Complete)
- Download dataset (Complete)
- Create data dictionary (Complete)

Questions:

- What tables exist? (Complete)
- What does each table represent? (Complete)
- Potential primary keys? (Complete)
- Potential foreign keys? (Complete)
- Interesting columns? (Complete)

Output:

docs/data_dictionary.md (Complete)

---

## Day 2

Business Understanding

Tasks:
- Investigate the data using SQL to verfy day1's hypothesis 

Questions:

- What type of company created this data?
- How does an order flow through the business?
- How do customers interact with products?
- What role do sellers play?

Output:

docs/business_questions.md

---

## Day 3

SQL Exploration

Answer:

- Total customers
- Total products
- Total sellers
- Total orders
- Product categories

Output:

sql/exploration/day3_exploration.sql

---

## Day 4

Aggregations

Answer:

- Revenue by month
- Orders by month
- Orders by state

Output:

sql/analysis/revenue_analysis.sql

---

## Day 5

Joins

Answer:

- Top customers
- Top products
- Top categories

Output:

sql/analysis/customer_product_analysis.sql

---

## Day 6

Project Consolidation

Create:

business_questions.sql

Include:

- Revenue trends
- Customer trends
- Product trends

---

## Day 7

Review Day

Tasks:

- Refactor queries
- Update README
- Update career log
- Commit all changes

---

# Week 2

Goal:

Strengthen SQL and begin data modeling.

Topics:

- LEFT JOIN
- CTEs
- Subqueries
- Date Functions
- Basic Window Functions

Deliverable:

First dimensional model draft.

---

## Day 8

LEFT JOIN

Questions:

- Customers without orders
- Products without sales

---

## Day 9

CTEs

Refactor existing queries.

---

## Day 10

Subqueries

Questions:

- Customers above average spend
- Products above average sales

---

## Day 11

Date Analysis

Questions:

- Monthly growth
- Quarterly trends

---

## Day 12

Ranking

Learn:

- ROW_NUMBER()
- RANK()

Questions:

- Top customers
- Top products

---

## Day 13

Dimensional Modeling

Learn:

- Fact Tables
- Dimension Tables

Create initial star schema draft.

---

## Day 14

Documentation

Update:

- README
- Data Dictionary
- Business Questions

---

# Week 3

Goal:

Design warehouse structure.

Topics:

- Star Schema
- Data Grain
- Fact and Dimension Design

Deliverables:

- Star schema
- Architecture diagram

---

## Day 15

Design fact_orders

---

## Day 16

Design dim_customers

---

## Day 17

Design dim_products

---

## Day 18

Design dim_date

---

## Day 19

Relationship Review

---

## Day 20

Documentation

---

## Day 21

Architecture Diagram

---

# Week 4

Goal:

Introduce Snowflake

Deliverables:

- Snowflake environment
- Raw layer
- Staging layer
- Analytics layer

---

## Day 22

Snowflake Setup

---

## Day 23

Data Loading

---

## Day 24

Raw Schema

---

## Day 25

Staging Schema

---

## Day 26

Analytics Schema

---

## Day 27

Data Movement Validation

---

## Day 28

Documentation

---

# Week 5

Goal:

Build dbt Models

Deliverables:

- Staging Models
- Fact Models
- Dimension Models

---

## Day 29

dbt Setup

---

## Day 30

stg_orders

---

## Day 31

stg_customers

---

## Day 32

fct_orders

---

## Day 33

dim_customers

---

## Day 34

dim_products

---

## Day 35

dbt Tests

- Not Null
- Unique
- Relationship Tests

---

# Week 6

Goal:

Create a recruiter-ready project.

Deliverables:

- Dashboard
- Documentation
- Screenshots
- Portfolio Quality Repository

---

## Day 36

Power BI Setup

---

## Day 37

Revenue Dashboard

---

## Day 38

Customer Dashboard

---

## Day 39

Product Dashboard

---

## Day 40

Capture Screenshots

---

## Day 41

Write Documentation

Sections:

- Problem
- Dataset
- Architecture
- Metrics
- Data Model

---

## Day 42

Final Review

Checklist:

- README complete
- Architecture diagram complete
- Star schema documented
- SQL organized
- dbt models documented
- Dashboard screenshots added
- GitHub repository cleaned up

---

# Current Status

## Completed

- GitHub repository created
- Local repository cloned
- Folder structure created
- Git workflow configured
- Raw data excluded from Git
- Initial documentation structure created