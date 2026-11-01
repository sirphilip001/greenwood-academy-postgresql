# Greenwood Academy PostgreSQL Database Project

A beginner-friendly PostgreSQL project for practicing database creation, table changes, sample data management, filtering, and basic analysis with a fictional secondary-school dataset.

## Project overview

The SQL script builds a `greenwood_academy` schema with three tables:

| Table | Purpose |
| --- | --- |
| `students` | Student names, gender, date of birth, class, and city |
| `subjects` | Subject names, departments, teachers, and credit hours |
| `exam_results` | Student marks, exam dates, and recorded grades |

The script inserts sample records for 10 students, 10 subjects, and 10 exam results, then demonstrates updates and a deletion. It includes 30 numbered exercises covering:

- Creating a schema and tables, then altering table columns
- Inserting, updating, and deleting records
- Selecting and filtering rows with `WHERE`, `AND`, `OR`, and comparison operators
- Searching and matching values with `BETWEEN`, `IN`, `NOT IN`, and `LIKE`
- Counting records with `COUNT`
- Categorizing marks and students with `CASE`

## Repository contents

```text
.
├── README.md
└── greenwood_academy.sql
```

## Requirements

- PostgreSQL
- `psql`, pgAdmin, DBeaver, or another PostgreSQL-compatible SQL client

## Run the script

The script creates the `greenwood_academy` schema inside the database you connect to. For example, create a practice database and run the script with `psql`:

```bash
createdb greenwood_practice
psql -d greenwood_practice -f greenwood_academy.sql
```

Alternatively, connect to an existing practice database in `psql` and run:

```text
\i /path/to/greenwood_academy.sql
```

In a graphical SQL client, open the script, connect to a practice database, and execute it there.

> **Run once in a disposable database.** This is a sequential learning script, not a migration designed for repeated execution. It creates the schema without `IF NOT EXISTS`, inserts fixed IDs, drops the temporary `phone_number` column, updates records, and deletes exam result `9`. Running it again in the same database will fail or encounter existing data.

## Data model

The tables use primary keys (`student_id`, `subject_id`, and `result_id`). Exam results contain student and subject IDs that refer to rows in the other tables, but the current script does not define foreign-key constraints. It also does not enforce mark ranges or calculate grades automatically; grades are inserted as sample values.

## Learning notes

This repository is an educational exercise using fictional sample data. The script demonstrates basic table structure and query patterns rather than a production-ready school information system.

`

