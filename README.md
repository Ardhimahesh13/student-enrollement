# Innomatics Student Enrollment System

A simple student enrollment management system built using Microsoft Access. This project provides a basic framework to manage student information and their enrollment in various courses.

## 🚀 Features

-   **Student Data Management**: Store and manage essential student details like name, contact information, date of birth, and gender.
-   **Course Catalog**: Maintain a list of available courses with unique IDs.
-   **Enrollment Tracking**: Easily enroll students into specific courses.
-   **User-Friendly Form**: A dedicated form for easy data entry, navigation, and saving records.
-   **Reporting**: A pre-built report to view student enrollments, conveniently grouped by course.

## 🗃️ Database Schema

The database consists of two main tables with a one-to-many relationship.

### Tables

#### **`Tb1Students`**
This table stores all information related to the students.

| Field             | Data Type | Key/Index      | Description                               |
| ----------------- | --------- | -------------- | ----------------------------------------- |
| `StudentID`       | AutoNumber| **Primary Key**| Unique identifier for each student.       |
| `FullName`        | Short Text| Indexed        | The full name of the student.             |
| `EnrollmentDate`  | Date/Time | -              | The date the student was enrolled.        |
| `PhoneNumber`     | Short Text| -              | The student's contact number.             |
| `EmailID`         | Short Text| Indexed        | The student's email address.              |
| `DOB`             | Date/Time | -              | The student's date of birth.              |
| `Gender`          | Short Text| -              | The gender of the student.                |
| `CourseID_FK`     | Number    | **Foreign Key**| Links to the `CourseID` in `Tb1Courses`. |

#### **`Tb1Courses`**
This table stores all available courses.

| Field        | Data Type  | Key/Index      | Description                           |
| ------------ | ---------- | -------------- | ------------------------------------- |
| `CourseID`   | AutoNumber | **Primary Key**| Unique identifier for each course.    |
| `CourseName` | Short Text | Indexed        | The name of the course.               |

### Relationship

A **one-to-many relationship** is established from `Tb1Courses` to `Tb1Students` using the `CourseID` field. This allows one course to have multiple students enrolled.

## 🏛️ Database Objects

The Access database is composed of the following objects:

* **Tables**:
    * `Tb1Students`
    * `Tb1Courses`
* **Query**:
    * `student enrllement with course name`: Joins the student and course tables to display details together.
* **Form**:
    * `Student Enrollment Form`: The main interface for data entry and management.
* **Report**:
    * `Student Enrollment by Course`: A summary report of enrollments, grouped by course.

## ⚙️ How to Use

1.  **Prerequisites**: You must have **Microsoft Access** installed on your computer.
2.  **Download**: Clone this repository or download the `Innomatics Enrollement.accdb` file.
3.  **Open**: Double-click the `.accdb` file to open it with Microsoft Access.
4.  **Enable Content**:
    > **Important:** If a security warning appears below the ribbon, click **Enable Content**. This is necessary to ensure that all macros and database functionalities work correctly.
5.  **Navigate the System**:
    * Use the **`Student Enrollment Form`** from the navigation pane to add new students or browse existing records.
    * Open the **`Student Enrollment by Course`** report to view or print the enrollment summary.

## 💻 Technology Used

* **Database**: Microsoft Access
