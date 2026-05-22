# day6-triggers-soql

## 1. What is SOQL?

SOQL (Salesforce Object Query Language) is used to retrieve data from Salesforce objects. It is similar to SQL but works specifically with Salesforce data.

Example:

SELECT Name FROM Student__c

This query retrieves student names from the Student object.

---

## 2. What is an Apex Trigger?

An Apex Trigger is a piece of code that automatically runs before or after events happen in Salesforce.

Examples of events:
- Insert
- Update
- Delete

Triggers help automate business processes.

Example:
When an Opportunity becomes Closed Won, automatically create a follow-up task.

---

## 3. Difference Between Flow and Trigger

| Flow | Apex Trigger |
|------|------|
| Declarative (No code) | Programmatic (Code) |
| Easy to build | Requires Apex coding |
| Best for simple automation | Best for complex logic |
| Faster development | More flexible |
| Used by admins | Used by developers |

### Example
- Sending simple email → Flow
- Complex fee calculation → Trigger

---

## 4. Difference Between Before Trigger and After Trigger

| Before Trigger | After Trigger |
|------|------|
| Runs before saving record | Runs after saving record |
| Used to update fields | Used for related actions |
| Faster because no extra save | Used when record ID is needed |

### Example
- Copy billing address → Before Trigger
- Create related task → After Trigger

---

# 5. Trigger Use Cases

## 1. Student Registration

### Event:
After student record is inserted.

### Action:
Send welcome email to student.

### Why?
To confirm successful registration automatically.

---

## 2. Attendance Warning

### Event:
After attendance percentage is updated.

### Action:
Send warning notification if attendance drops below 75%.

### Why?
To alert students early.

---

## 3. Course Full Alert

### Event:
After maximum student limit is reached.

### Action:
Notify faculty and stop further registrations.

### Why?
To manage classroom capacity.

---

## 4. Fee Payment Completion

### Event:
After fee status becomes "Paid".

### Action:
Generate payment receipt automatically.

### Why?
To reduce manual work.

---

## 5. Exam Result Published

### Event:
After exam results are inserted.

### Action:
Send result notification to students.

### Why?
To provide instant updates.

---

# 6. Query Examples

## Find all students in Course A

SELECT Name FROM Student__c WHERE Course__c = 'Course A'

---

## Find all courses handled by Faculty X

SELECT Name FROM Course__c WHERE Faculty__c = 'Faculty X'

---

## Find students with attendance below 75%

SELECT Name FROM Student__c WHERE Attendance__c < 75

---

## Find students who paid fees

SELECT Name FROM Student__c WHERE Fee_Status__c = 'Paid'

---

## Find all active courses

SELECT Name FROM Course__c WHERE Status__c = 'Active'

---

# 7. Reflection

## Why do enterprise systems react automatically to data changes?

Enterprise systems handle large amounts of data and users every day. Manual monitoring is slow and inefficient.

Automatic reactions help:
- Save time
- Reduce human errors
- Improve business efficiency
- Send instant notifications
- Keep records updated automatically

Event-driven behavior makes systems intelligent and responsive.

Example:
When a customer places an order, the system can automatically:
- Update inventory
- Generate invoice
- Send confirmation email

Without automation, these tasks would require manual work.

---
## Database & .NET Basics
![Database & .NET Basics](<Screenshot 2026-05-22 205831.png>)
## Apex Triggers
![Apex Triggers](<Screenshot 2026-05-22 205802.png>)