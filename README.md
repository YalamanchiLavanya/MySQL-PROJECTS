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
├── Student Mangement.jpg
└── README.md
```

---

## 📌 Conclusion

The **Student Management System** demonstrates how relational databases can be used to manage student academic information efficiently. The project connects students, subjects, exams, and marks using primary and foreign key relationships and provides SQL queries ranging from basic data retrieval to advanced aggregation and conditional logic.




# 🌱 Cashew Management System

## 📌 Overview

The **Cashew Management System** is a database management project designed to manage and organize information related to cashew farming. The system stores details about farmers, farms, harvesting, sales, workers, fertilizers, expenses, equipment, irrigation, pest control, and government subsidies.

The main goal of this project is to help manage farming activities efficiently and maintain accurate records in a structured database.

## 🎯 Objectives

* Manage farmer and farm information.
* Maintain land and cultivation details.
* Record cashew harvesting activities.
* Manage cashew sales and buyers.
* Maintain worker information.
* Track fertilizer usage.
* Record farming expenses.
* Manage farming equipment.
* Track irrigation activities.
* Manage pest-control activities.
* Provide information about government subsidies.
* Generate useful information using SQL queries.

## 🗂️ Main Tables

### 1. Farmers

Stores information about farmers.

**Important attributes:**

* `FarmerID` – Primary Key
* `FarmerName`
* `Phone`
* `Village`
* `District`

### 2. Farms

Stores information about agricultural land.

**Important attributes:**

* `FarmID` – Primary Key
* `FarmerID` – Foreign Key
* `LandArea`
* `Location`
* `SoilType`
* `CashewVariety`

### 3. Harvest

Stores details about cashew production.

**Important attributes:**

* `HarvestID` – Primary Key
* `FarmID` – Foreign Key
* `HarvestDate`
* `QuantityKg`
* `Grade`
* `Season`

### 4. Sales

Stores information about cashew sales.

**Important attributes:**

* `SaleID` – Primary Key
* `HarvestID` – Foreign Key
* `BuyerName`
* `SaleDate`
* `QuantityKg`
* `PricePerKg`
* `TotalAmount`

### 5. Workers

Stores information about workers involved in farming activities.

### 6. Fertilizers

Stores fertilizer usage and application details.

### 7. Expenses

Stores different expenses related to cashew farming.

### 8. Equipment

Stores information about agricultural equipment.

### 9. Irrigation

Stores irrigation activities and water-management details.

### 10. Pest Control

Stores information about pest-control activities and treatments.

### 11. Government Subsidies

Stores available government subsidy information and farmer applications.

## 🔗 Relationships

The database uses **Primary Keys (PK)** and **Foreign Keys (FK)** to connect related tables.

Examples:

Farmers
   1
   |
   N
 Farms

One farmer can own multiple farms.

Farms
   1
   |
   N
Harvest


One farm can have multiple harvest records.

Harvest
   1
   |
   N
Sales


Harvest information can be associated with sales records.

Other relationships connect farms with:

* Workers
* Fertilizers
* Expenses
* Equipment
* Irrigation
* Pest Control
* Government Subsidies

## 🧩 ER Diagram Components

The ER diagram represents:

* **Strong Entities**
* **Attributes**
* **Primary Keys**
* **Foreign Keys**
* **Relationships**
* **Cardinality**
* **Composite Attributes**
* **Derived Attributes**
* **Weak Entities**, where applicable

## 💾 Database Technology

**Database:** MySQL

**Tools:**

* MySQL Workbench
* SQL
* Draw.io / diagrams.net for ER diagrams

## 🔍 SQL Operations

The project supports different levels of SQL queries.

### Basic Queries

* Retrieve farmer details.
* Display all farms.
* Find farms by location.
* Display harvest records.
* Find farmers from a particular village.

### Intermediate Queries

* Use `JOIN` operations between tables.
* Calculate total harvest quantity.
* Calculate total sales.
* Find average selling price.
* Group farmers based on location.

### Advanced Queries

* Subqueries
* Aggregate functions
* Multiple-table joins
* `GROUP BY`
* `HAVING`
* Views
* Nested queries

## 🌾 Benefits

* Centralized management of farming data.
* Easy tracking of land and cultivation activities.
* Better monitoring of production and sales.
* Helps farmers track expenses.
* Provides information about subsidies.
* Reduces duplicate and unorganized records.
* Makes data retrieval faster using SQL queries.
* Can be extended into a web-based farming management application.

## 🚀 Future Enhancements

The system can be extended with:

* Farmer login and registration.
* Online government subsidy applications.
* Real-time market price information.
* Weather information.
* Crop disease detection.
* Mobile application.
* Farmer dashboard.
* Sales and profit analysis.
* Data visualization using Power BI or Tableau.
* Python-based backend.
* Web-based user interface.

## 📁 Project Structure

Cashew-Management-System/
│
├── README.md
├── database/
│   ├── create_tables.sql
│   └── queries.sql
│
├── er-diagram/
│   └── cashew_management_er_diagram.png


## 👩‍💻 Project Summary

The **Cashew Management System** is a practical database project that demonstrates how SQL and database concepts can be applied to real-world agricultural management. It provides a structured way to manage cashew farming operations from land management and cultivation to harvesting, sales, expenses, and government support.
