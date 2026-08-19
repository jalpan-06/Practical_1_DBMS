# Student Database Management

A simple SQL project that demonstrates the creation of a `Student` table and insertion of sample student records. This project serves as a basic example of Data Definition Language (DDL) and Data Manipulation Language (DML) operations in SQL.

## Overview

The database stores information about students, including:

* Student ID
* Student Name
* Department

This project can be used as a beginner-friendly reference for learning SQL table creation and data insertion.

## Database Schema

### Student Table

| Column Name | Data Type   | Description                     |
| ----------- | ----------- | ------------------------------- |
| Student_Id  | INT         | Unique identifier for a student |
| Name        | VARCHAR(20) | Student's name                  |
| Dept        | VARCHAR(15) | Department of the student       |

## SQL Script

```sql id="c9r7m8"
CREATE TABLE Student(
    Student_Id INT,
    Name VARCHAR(20),
    Dept VARCHAR(15)
);

INSERT INTO Student (Student_Id, Name, Dept)
VALUES
    (1, 'Reet', 'CSE'),
    (2, 'Jay', 'Civil');
```

## Sample Data

| Student_Id | Name | Dept  |
| ---------: | ---- | ----- |
|          1 | Reet | CSE   |
|          2 | Jay  | Civil |

## Getting Started

### Prerequisites

* MySQL, PostgreSQL, SQL Server, Oracle Database, or any SQL-compatible RDBMS
* SQL Query Editor (MySQL Workbench, pgAdmin, SSMS, DBeaver, etc.)

### Installation

1. Clone the repository:

```bash id="t6m5n4"
git clone https://github.com/your-username/student-database.git
```

2. Open your preferred SQL database environment.

3. Execute the SQL script to create the table and insert sample records.

## Usage

Retrieve all student records:

```sql id="l3k2j1"
SELECT * FROM Student;
```

### Expected Output

```text id="h8g7f6"
+------------+------+-------+
| Student_Id | Name | Dept  |
+------------+------+-------+
| 1          | Reet | CSE   |
| 2          | Jay  | Civil |
+------------+------+-------+
```

## Project Structure

```text id="d4s3a2"
student-database/
│
├── student.sql
└── README.md
```

## Future Enhancements

* Add a Primary Key constraint on `Student_Id`
* Implement `NOT NULL` constraints
* Add additional attributes such as Email, Age, and Semester
* Create relationships with other tables (Courses, Faculty, Enrollment)
* Implement indexing for improved query performance

## Best Practice Recommendation

For better data integrity, consider defining the table as:

```sql id="p0o9i8"
CREATE TABLE Student (
    Student_Id INT PRIMARY KEY,
    Name VARCHAR(20) NOT NULL,
    Dept VARCHAR(15) NOT NULL
);
```

## License

This project is available under the MIT License. Feel free to use, modify, and distribute it for educational and learning purposes.

## Author

**Jalpan Bhavesh Mandavia**

SQL Database Practice Project
