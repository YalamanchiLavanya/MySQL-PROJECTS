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


# 🌱 AgriCashew Management System

## 📌 About the Project
The **AgriCashew Management System** is a MySQL-based database project designed to manage and organize information related to **cashew farming and agricultural activities**.
The main purpose of this project is to provide a centralized database where information about **farmers, buyers, farms, harvests, farming equipment, cashew prices, weather conditions, requests, connections, and ratings** can be stored and managed efficiently.
Farmers can maintain their farm and harvest information, while buyers can view farmer-related information and interact with them for business purposes. The system also supports **equipment requests**, allowing users to manage farming equipment and requests.
The project also includes **cashew price management**, which helps store market prices according to quality and date. Weather information can also be maintained to support better farming decisions.
An important part of the system is the **connection between farmers and buyers**. Users can send contact requests and interact with other users. The rating system allows farmers and buyers to provide feedback and build trust with each other.
The database is designed using **Primary Keys and Foreign Keys** to maintain relationships between different tables and avoid unnecessary duplication of data.
SQL queries are used to retrieve and analyze the stored information. The project includes queries using **SELECT, WHERE, ORDER BY, JOIN, GROUP BY, HAVING, aggregate functions, subqueries, CASE statements, and self joins**.
Overall, the AgriCashew Management System provides a structured database solution for managing cashew farming information and improving interaction between **farmers and buyers**.

## 🎯 Objectives
- Manage farmer and buyer information
- Store farm details
- Track cashew harvests
- Manage farming equipment
- Store cashew market prices
- Store weather information
- Allow farmers and buyers to connect
- Manage equipment requests
- Provide ratings and reviews
## 🗄️ Database Name

```sql
agricashew
📋 Database Tables
===================
The project contains the following tables:
Users
Farmers
Buyers
Farms
Harvests
Equipment
Equipment Requests
Contact Requests
Cashew Prices
Weather
Buyer Ratings
Farmer Ratings

🔗 Relationships
====================
The main relationships between the tables are:
Users → Farmers : One-to-One
Users → Buyers : One-to-One
Farmers → Farms : One-to-Many
Farms → Harvests : One-to-Many
Farmers → Equipment : One-to-Many
Equipment → Equipment Requests : One-to-Many
Buyers → Equipment Requests : One-to-Many
Farmers → Buyer Ratings : One-to-Many
Buyers → Farmer Ratings : One-to-Many

🧩 ER Diagram
===============
The ER diagram represents the structure of the AgriCashew database.
Main Entities
==============
Users
Farmers
Buyers
Farms
Harvests
Equipment
Equipment Requests
Contact Requests
Cashew Prices
Weather
Buyer Ratings
Farmer Ratings

ER Diagram Symbols
===================
Rectangle → Entity
Ellipse → Attribute
Diamond → Relationship
PK → Primary Key
FK → Foreign Key
1 : 1 → One-to-One
1 : N → One-to-Many

📊 Main Features
==================
👨‍🌾 Farmer Management
Stores farmer information such as name, contact details, location, and farming experience.
🌾 Farm Management
Stores farm details such as farm name, location, area, and soil type.

🌰 Harvest Management
Stores information about cashew harvests including date, season, quantity, and quality.

🛠️ Equipment Management
Farmers can add and manage farming equipment and buyers can request available equipment.

💰 Cashew Price Management
Stores cashew market prices based on quality, date, and market location.

🌦️ Weather Management
Stores weather information such as temperature, rainfall, humidity, location, and date.

🤝 Farmer and Buyer Connection
Farmers and buyers can send contact requests and communicate with each other.

⭐ Ratings
Farmers and buyers can give ratings and reviews to each other.

🔍 SQL Queries
=================
The project contains SQL queries at Easy, Medium, and Hard levels.
🟢 Easy Queries
Display all farmers.
Find farmers with more than 5 years of experience.
Display Grade A harvests.
Display available equipment.
Find cashew prices greater than 800.
🟡 Medium Queries
Display farmer names and farm names.
Display farmer names with their harvest quantities.
Find the total harvest quantity of each farmer.
Find the average rating of each farmer.
Display equipment details with farmer names.
🔴 Hard Queries
Find the farmer with the highest total harvest.
Find farmers with an average rating greater than 4.
Find farmers who have both Grade A and Grade B harvests.
Calculate the estimated value of a harvest.
Display accepted contact requests between users.

🎯 SQL Concepts Used
This project helps practice:
=============================
SELECT
WHERE
ORDER BY
INNER JOIN
GROUP BY
HAVING
Aggregate Functions
SUM()
AVG()
COUNT()
Subqueries
CASE Statements
Self Join
Primary Keys
Foreign Keys

🛠️ Technologies Used
=======================
MySQL
MySQL Workbench
SQL
Draw.io

🚀 How to Run
===============
Open MySQL Workbench.
Create a new SQL file.
Create the agricashew database.
Select the database.
Create all required tables.
Insert the sample data.
Run the SQL queries.
Use SELECT * to check the data.

** 📁 Project Structure
==========================
AgriCashew-Management-System/
│
├── agricashew.sql
├── AgriCashew ER Diagram.drawio
└── README.md

📌 Conclusion
=================
The AgriCashew Management System is a MySQL-based database project designed to manage important cashew farming information in an organized way. It stores details about farmers, buyers, farms, harvests, equipment, cashew prices, weather conditions, requests, connections, and ratings in separate but related tables.
The project demonstrates the practical use of Primary Keys, Foreign Keys, table relationships, and SQL queries for managing and analyzing data. It includes SQL concepts such as SELECT, WHERE, ORDER BY, JOIN, GROUP BY, HAVING, aggregate functions, subqueries, CASE statements, and self joins.
Overall, AgriCashew provides a structured solution for managing cashew farming activities and improving interaction between farmers and buyers. The project can be further developed into a complete web or mobile application with features such as online cashew sales, notifications, dashboards, farming suggestions, weather-based recommendations, and price prediction.

## 👩‍💻 Author

**Name:** Lavanya Yalamanchi

## 📌 Project Name

**AgriCashew Management System**
