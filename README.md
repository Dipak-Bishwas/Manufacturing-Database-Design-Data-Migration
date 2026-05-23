# Manufacturing Database Design & Data Migration

## Project Overview
This project focuses on designing and implementing a relational database system for a manufacturing company using SQL Server and T-SQL. The existing manufacturing data was maintained in multiple Excel files, leading to data inconsistencies, duplicate records, scheduling conflicts, and inefficient reporting.

The project solves these operational challenges by building a normalized database structure and migrating manufacturing data into a centralized SQL-based system.

---

# Business Problem
The manufacturing company faced several operational issues due to spreadsheet-based data management:

- Lack of unique identifiers for suppliers, machines, materials, and production orders
- Inconsistent and duplicate data entries
- Invalid relationships between production orders and machines
- Machine scheduling conflicts
- Poor inventory traceability
- Difficulty generating production and quality reports
- Manual and inefficient reporting processes

This project was designed to solve these problems through proper database architecture, data cleaning, and migration techniques.

---

# Objectives
- Design a normalized relational database system
- Migrate manufacturing data from Excel-based datasets
- Ensure data consistency and integrity
- Implement production scheduling validation
- Improve inventory tracking and material traceability
- Manage quality inspections and production workflows
- Support future reporting and analytics requirements

---

# Technologies Used
- SQL Server
- T-SQL
- Relational Database Design
- Data Cleaning & Transformation
- Data Migration
- SQL Constraints
- SQL Triggers
- Common Table Expressions (CTEs)
- Joins and Aggregations

---

# Database Modules

## Supplier Management
Stores supplier details and raw material provider information.

## Customer Management
Maintains customer records and customer production orders.

## Raw Material Inventory
Tracks:
- Material batches
- Material grades
- Units
- Inventory quantities
- Supplier relationships

## Machine Management
Stores:
- Machine details
- Machine types
- Plant identifiers
- Maintenance history

## Production Orders
Handles:
- Production scheduling
- Machine assignments
- Production status tracking
- Customer order linkage

## Production Material Usage
Tracks raw material consumption for each production order.

## Employee Management
Stores employee and inspector information.

## Quality Check Management
Tracks:
- Quality inspections
- Inspection timestamps
- Inspection results
- Inspector assignments

---

# Key Features

## Relational Database Design
Implemented:
- Primary Keys
- Foreign Keys
- Unique Constraints
- Check Constraints
- Identity Columns

to maintain data integrity and enforce valid relationships.

---

## Data Cleaning & Standardization
Performed extensive data cleaning to standardize:
- Supplier names
- Material grades
- Measurement units
- Machine naming conventions
- Date formats

Used SQL functions such as:
- `CASE`
- `TRIM`
- `CAST`
- `CONVERT`
- `TRY_CONVERT`

---

## Data Migration
Migrated manufacturing data from raw Excel-based datasets into normalized relational tables while preserving:
- Historical records
- Referential integrity
- Production traceability

---

## Production Scheduling Validation
Implemented SQL Trigger logic to:
- Prevent overlapping machine schedules
- Improve production planning
- Reduce scheduling conflicts

---

## Inventory Management
Tracked:
- Initial material quantities
- Remaining inventory quantities
- Material usage across production orders

---

## Quality Control Integration
Integrated quality inspection workflows into production tracking using relational mappings between:
- Production orders
- Inspectors
- Inspection results

---

# Database Tables

| Table Name | Description |
|---|---|
| SUPPLIERS | Stores supplier information |
| CUSTOMERS | Stores customer details |
| RAWMATERIALS | Stores raw material information |
| MACHINES | Stores machine details |
| PRODUCTIONORDERS | Stores production scheduling data |
| MATERIALINVENTORY | Tracks raw material inventory |
| PRODUCTIOMATERIALUSAGE | Tracks material consumption |
| EMPLOYEES | Stores employee information |
| QUALITYCHECKS | Stores quality inspection records |

---

# Advanced SQL Concepts Used
- Joins
- CTEs
- Aggregate Functions
- Data Type Conversion
- Constraints
- Triggers
- Data Validation
- Referential Integrity
- Transaction Control

---

# Real-World Manufacturing Scenarios Solved

## Machine Double Booking Prevention
Implemented trigger-based validation to prevent assigning the same machine to overlapping production schedules.

## Failed Quality Inspection Handling
Automatically updated production status to:
- `Rework Required`

when inspection results failed.

## Inventory Tracking
Calculated and updated remaining inventory quantities after production material consumption.

---

---

# ER Diagram
The project includes an ER diagram illustrating:
- Table relationships
- Primary and foreign keys
- Manufacturing workflow mapping

---

# Future Improvements
- Role-Based Access Control (RBAC)
- Automated inventory alerts
- Advanced production analytics dashboards
- Supplier performance reporting
- Machine efficiency analysis
- Stored procedures for automation

---

# Learning Outcomes
Through this project, I gained hands-on experience in:
- Relational database design
- Data migration techniques
- SQL query optimization
- Data cleaning and transformation
- Manufacturing workflow modeling
- Trigger implementation
- Real-world production system design

---

