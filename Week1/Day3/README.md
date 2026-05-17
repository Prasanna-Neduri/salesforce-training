# Day 3 – Salesforce Data Modeling

# 1. Difference Between App, Object, Record, and Field

| Term | Explanation |
|---|---|
| App | A collection of related tabs, objects, and tools designed for a business purpose |
| Object | A database table used to store related data |
| Record | A single entry inside an object |
| Field | A single piece of information inside a record |

---

# Example

## App
College Management App

## Object
Student Object

## Record
Rahul Kumar

## Fields
- Student Name
- Email
- Department

---

# 2. Standard vs Custom Objects

## Standard Objects
Objects already provided by Salesforce.

### Examples
- Account
- Contact
- Opportunity

---

## Custom Objects
Objects created based on business requirements.

### Examples
- Student
- Faculty
- Course
- Department

---

# 3. College Management System Data Model

## Objects
1. Student
2. Faculty
3. Course
4. Department

---

# Relationships

## Department → Faculty
One department can have many faculty members.

## Department → Course
One department can offer multiple courses.

## Course → Student
One course can contain many students.

## Faculty → Course
One faculty member can teach multiple courses.

---

# Relationship Type
Lookup Relationships are used because objects remain independent.

---

# Data Model Diagram

```txt
Department
   │
   ├── Faculty
   │
   └── Course
            │
            └── Student
```


---

# 4. Formula Fields

## Full Name
Combines First Name and Last Name.

### Why?
Avoids repetitive manual entry.

---

## Remaining Seats
Total Seats - Enrolled Students

### Why?
Shows available seats automatically.

---

## Percentage
(Obtained Marks / Total Marks) * 100

### Why?
Reduces manual calculation errors.

---

# 5. Validation Rules

## Email Cannot Be Empty

### Prevents
Missing communication details.

---

## Student Age Cannot Be Negative

### Prevents
Invalid age values.

---

## Course Seats Cannot Exceed Limit

### Prevents
Overbooking.

---

# 6. Reflection – Why Structured Data Matters

Structured data:
- Improves organization
- Helps automation
- Reduces duplicate data
- Improves reporting
- Supports business decisions

Spreadsheets become difficult to manage when data grows large.

---
# screen shots
## Data Modeling
![Data Modeling](<Screenshot 2026-05-16 170033.png>)

## Formulas and Validations
![Formulas and Validations](<Screenshot 2026-05-17 183156.png>)