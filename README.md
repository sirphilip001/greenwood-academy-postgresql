Greenwood Academy — SQL Database & Querying Project
This repository contains a full PostgreSQL script (greenwood_academy.sql) covering core Data Definition Language (DDL), Data Manipulation Language (DML), and Data Querying tasks for a school database management system.

Project Overview
The project models a high school database for Greenwood Academy, tracking students, academic subjects, and examination performance across various forms.

Schema & Tables Structure
students: Personal details (names, gender, date of birth, class, city).

subjects: Course catalog (department, teacher, credit hours).

exam_results: Performance tracking (student scores, dates, grades).

Key Topics Covered
Database Setup & DDL (CREATE, ALTER, DROP)

Schema creation and search path configuration.

Table design with PRIMARY KEY, NOT NULL, and UNIQUE constraints.

Modifying table structures via column addition, renaming, and deletion.

Data Manipulation & Maintenance (INSERT, UPDATE, DELETE)

Populating initial mock records for students, subjects, and exam results.

Updating record attributes (city relocation, mark corrections).

Removing cancelled records.

Data Analysis & Filtering (WHERE, Operators, Pattern Matching)

Conditional logic (AND, OR, NOT IN).

Range filtering (BETWEEN).

Text pattern matching (LIKE wildcard searches).

Aggregations (COUNT).

Conditional classification (CASE WHEN expressions for performance labeling).

How to Run the Script
Prerequisites
PostgreSQL installed and running locally.

Access to psql shell or a SQL GUI client (DBeaver, pgAdmin, VS Code PostgreSQL extension).

Execution Instructions via psql
Open your terminal and connect to PostgreSQL:

Bash
psql -U postgres -d postgres
Run the script directly from your directory:

SQL
\i greenwood_academy.sql
