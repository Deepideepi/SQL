# SQL

This project is based on the students course details

Training Institute Database

This project represents a database system for a training institute, consisting of four main entities: Instructors, Courses, Students, and Enrollments. Each table stores essential information and is linked appropriately using primary keys (PK) and foreign keys (FK).

1️⃣ Instructors Table

Stores details about instructors who teach courses.

Columns

Instructor_ID (PK)

Full_name

Email (must be unique)

Salary

2️⃣ Courses Table

Contains information about the courses offered in the institute.

Columns

Course_ID (PK)

Course_name

Duration_months

Instructor_ID (FK → Instructors.Instructor_ID)

Each course is assigned to one instructor.

3️⃣ Students Table

Stores data about students enrolled in the institute.

Columns

Student_ID (PK)

Full_name

Email (unique constraint)

Join_date

4️⃣ Enrollments Table

Represents the many-to-many relationship between Students and Courses.

Columns

Enroll_ID (PK)

Student_ID (FK → Students.Student_ID)

Course_ID (FK → Courses.Course_ID)

Enroll_date

Status

Each enrollment links one student to one course.

Additional Notes

Email fields (Students and Instructors) are marked as NOT NULL and UNIQUE.

Relationship flow:

Instructor → teaches → Course

Student → enrolls in → Course

Example mentioned: showing Course Name + Student Name will require a 2-column display, likely through a JOIN.
