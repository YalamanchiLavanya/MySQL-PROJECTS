# MySQL-PROJECTS
This MySQL project demonstrates database design and SQL query operations using multiple related tables. It covers selection, filtering, sorting, joins, aggregation, subqueries, grouping, HAVING, CASE statements, and practical data analysis queries for calculating averages, counting records, finding top scores, and generating performance reports.

# Student Management System – MySQL

## 📌 Project Overview

The **Student Management System** is a MySQL database project designed to store and manage student information, subjects, exams, and marks.

The database uses multiple related tables with **Primary Keys (PK)** and **Foreign Keys (FK)** to maintain relationships between students, subjects, exams, and their marks.

---

## 🗄️ Database Name

```sql
studentdb
```

---

## 📋 Tables

### 1. Students

Stores the basic information of students.

| Column          | Data Type   | Key         |
| --------------- | ----------- | ----------- |
| student_id      | INT         | Primary Key |
| first_name      | VARCHAR(50) |             |
| last_name       | VARCHAR(50) |             |
| enrollment_year | INT         |             |

### 2. Subjects

Stores the subjects offered to students.

| Column       | Data Type   | Key         |
| ------------ | ----------- | ----------- |
| subject_id   | INT         | Primary Key |
| subject_name | VARCHAR(50) |             |

### 3. Exams

Stores information about different examinations.

| Column    | Data Type   | Key         |
| --------- | ----------- | ----------- |
| exam_id   | INT         | Primary Key |
| exam_name | VARCHAR(50) |             |
| exam_date | DATE        |             |

### 4. Marks

Stores the marks obtained by students in different subjects and exams.

| Column     | Data Type | Key         |
| ---------- | --------- | ----------- |
| mark_id    | INT       | Primary Key |
| student_id | INT       | Foreign Key |
| subject_id | INT       | Foreign Key |
| exam_id    | INT       | Foreign Key |
| score      | INT       |             |

---

## 🔗 Relationships

The database contains the following relationships:

| Relationship     | Cardinality | Description                     |
| ---------------- | ----------- | ------------------------------- |
| Students → Marks | 1 : N       | One student can have many marks |
| Subjects → Marks | 1 : N       | One subject can have many marks |
| Exams → Marks    | 1 : N       | One exam can have many marks    |

The **Marks** table acts as the central table connecting **Students, Subjects, and Exams**.

---

## 🧩 ER Diagram

The ER diagram uses standard ER-model symbols:

* **Rectangle** → Entity
* **Ellipse** → Attribute
* **Diamond** → Relationship
* **PK** → Primary Key
* **FK** → Foreign Key
* **1 : N** → One-to-Many relationship

### Entities

* Students
* Subjects
* Exams
* Marks

### Relationships

* Students **HAS** Marks
* Subjects **HAS** Marks
* Exams **CONTAINS** Marks

---

## 📊 Sample Data

The database contains sample records for:

* **4 Students**
* **3 Subjects**
* **2 Exams**
* **8 Marks**

### Students

| ID | Name         | Enrollment Year |
| -: | ------------ | --------------: |
|  1 | Aarav Sharma |            2023 |
|  2 | Diya Patel   |            2023 |
|  3 | Vihaan Rao   |            2024 |
|  4 | Ananya Singh |            2024 |

### Subjects

|  ID | Subject          |
| --: | ---------------- |
| 101 | Mathematics      |
| 102 | Science          |
| 103 | Hindi Literature |

### Exams

| ID | Exam              | Date       |
| -: | ----------------- | ---------- |
|  1 | Half-Yearly 2024  | 2024-09-15 |
|  2 | Final Annual 2024 | 2024-03-20 |

---

## 🔍 SQL Practice Queries

The project includes SQL queries at three difficulty levels.

### Level 1 – Simple

1. Retrieve all students.
2. Find marks where the score is greater than 80.
3. Sort exams by date.

### Level 2 – Intermediate

4. Display student name, subject name, and score using joins.
5. Calculate the average score for each subject.
6. Count the number of marks recorded for Aarav Sharma.

### Level 3 – Complex

7. Find the student with the highest single score.
8. Find exams where the total score is greater than 250.
9. Display Pass/Fail status based on the score.

---

## 🎯 Learning Objectives

This project helps practice:

* Database creation
* Table creation
* Primary Keys
* Foreign Keys
* Relationships
* Data insertion
* SELECT queries
* WHERE conditions
* ORDER BY
* INNER JOIN
* Aggregate functions
* GROUP BY
* HAVING
* Subqueries
* CASE statements

---

## 🛠️ Technologies Used

* **MySQL**
* **MySQL Workbench**
* **SQL**

---

## 🚀 How to Run

1. Open **MySQL Workbench**.
2. Create a new SQL query.
3. Run the database creation command.
4. Select the `studentdb` database.
5. Create the required tables.
6. Insert the sample data.
7. Execute the practice queries.
8. Use `SELECT *` statements to verify the inserted data.

---

## 📁 Project Structure

```text
Student-Management-System/
│
├── student_management.sql
├── ER_Diagram.png
└── README.md
```

---

## 📌 Conclusion

The **Student Management System** demonstrates how relational databases can be used to manage student academic information efficiently. The project connects students, subjects, exams, and marks using primary and foreign key relationships and provides SQL queries ranging from basic data retrieval to advanced aggregation and conditional logic.
