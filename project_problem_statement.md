# Manufacturing Database Creation and Data Migration

## Background
Our manufacturing company produces industrial machinery components. Currently, all records—including raw materials inventory, supplier details, production schedules, machine maintenance logs, quality assurance checks, and customer orders—are managed using a collection of Excel files.

As operations expanded, this approach became inefficient, leading to:
- Data entry errors
- Duplicate records
- Production delays
- Difficulty generating accurate reports for decision-making

To improve data integrity, traceability, and operational efficiency, the company decided to migrate all operational data into a structured relational database system.

---

# Problem Description
The objective of this project is to design and build a robust relational database system capable of managing all core manufacturing operations.

The system must:
- Analyze existing Excel-based data
- Design normalized relational tables
- Establish relationships between entities
- Migrate existing operational data
- Maintain data integrity and consistency
- Preserve historical manufacturing records

---

# Business Problems Solved

## 1. Lack of Unique Identifiers
### Current Issue
There were no guaranteed unique identifiers for:
- Raw material batches
- Suppliers
- Machines
- Production orders
- Components

This created difficulties in tracing manufactured components back to their source materials.

### Solution
Implemented:
- Primary Keys
- Identity Columns
- Unique Constraints

to ensure unique identification across all entities.

---

## 2. Disconnected Relationships
### Current Issue
Production orders in Excel referenced machines and raw materials without enforcing valid relationships.

This caused:
- Scheduling on unavailable machines
- Incorrect material usage
- Invalid production references

### Solution
Implemented:
- Foreign Key Relationships
- Referential Integrity Constraints

to ensure valid links between:
- Production Orders
- Machines
- Raw Materials
- Inventory
- Customers

---

## 3. Invalid and Ambiguous Data Entries
### Current Issue
Data inconsistencies existed such as:
- `SS-304` vs `Stainless 304`
- `Kg` vs `KG`
- Different date formats
- Inconsistent supplier naming

### Solution
Performed:
- Data Cleaning
- Data Standardization
- Transformation Logic
- Validation Rules

using SQL functions such as:
- `CASE`
- `TRIM`
- `CAST`
- `CONVERT`
- `TRY_CONVERT`

---

## 4. Unregulated Production Scheduling
### Current Issue
Machines were frequently double-booked for overlapping production schedules.

Production was also scheduled without checking raw material availability.

### Solution
Implemented:
- Check Constraints
- SQL Triggers
- Scheduling Validation Logic

to:
- Prevent overlapping machine schedules
- Validate production timelines
- Support inventory-based production planning

---

## 5. Open Access to Sensitive Production Data
### Current Issue
All staff members had unrestricted access to:
- Production schedules
- Supplier information
- Material costs
- Customer orders

### Solution
Designed the foundation for:
- Role-Based Access Control (RBAC)

Examples:
- Operators can access assigned tasks only
- Supervisors can monitor production lines
- Procurement teams can access supplier details

---

## 6. Disconnected Reporting and Analytics
### Current Issue
Generating reports required manually combining multiple Excel files.

### Solution
Designed a centralized relational database capable of supporting:
- Machine efficiency reporting
- Raw material consumption analysis
- Supplier quality analysis
- Production tracking reports
- Quality inspection reporting

---

# Technologies Used
- SQL Server
- T-SQL
- Relational Database Design
- Data Migration Techniques
- Data Cleaning & Transformation
- SQL Constraints
- SQL Triggers
- Joins and CTEs

---

# Key Features
- Normalized database structure
- Data migration from Excel datasets
- Inventory management
- Production scheduling
- Machine allocation tracking
- Quality inspection management
- Supplier and customer management
- Trigger-based scheduling validation
- Manufacturing workflow integration
