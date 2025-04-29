# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Student Name

## Scenario Chosen:
University

## ER Diagram:
![image](https://github.com/user-attachments/assets/5d23311f-a90d-4a38-b1e3-57353b8b673d)


## Entities and Attributes:
- UNIVERSITY -
Tier,Location,DEPARTMENT,Department_ID,Department_Name,HOD

- COURSES -
Course_Name,Course_Code,Credits,Pre-requisite

- PROFESSOR -
ID,Name,Mail_ID,Phone_Number

- STUDENT -
Student_ID,Student_Name,Mail_ID,Phone_Number,DOB,Address
...

## Relationships and Constraints:
- UNIVERSITY — HAS —> DEPARTMENT
Cardinality: One-to-Many (One university has many departments)
Participation: Total (Each department must belong to a university)

- UNIVERSITY — HAS —> PROFESSOR
Cardinality: One-to-Many
Participation: Total

- DEPARTMENT — OFFERS —> COURSES
Cardinality: One-to-Many (A department offers multiple courses)
Participation: Total (Every course is offered by some department)

- PROFESSOR — TAUGHT —> COURSES
Cardinality: Many-to-Many (Professors can teach multiple courses and courses can be taught by multiple professors)
Participation: Partial (Not all professors may be teaching at a given time)

- COURSES — ENROLLED BY —> STUDENT
Cardinality: Many-to-Many (Many students can enroll in many courses)
Participation: Partial (Some students may not be enrolled in any course)
...

## Extension (Prerequisite):
- The "Pre-requisite" attribute in the COURSES entity is modeled to indicate that a course may require completion of another course beforehand. This is kept as a single attribute for simplicity but can be extended into a self-referential relationship for complex prerequisite chains.

## Design Choices:
Entities such as Department, Course, Student, Professor, and University are chosen to reflect real-world university components.
Relationships like "Offers", "Taught", and "Enrolled By" were included to model academic structure and course enrollment.
Many-to-Many relationships are used where appropriate (e.g., course enrollments, teaching assignments).
Pre-requisite is represented as an attribute for simplicity but can be normalized into a separate relationship if needed.

## RESULT
Thus the ER daigram have been successfully drawn and explained briefly.
