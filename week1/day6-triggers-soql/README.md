# Day 6 – Triggers and SOQL

## 1. What is SOQL?

SOQL (Salesforce Object Query Language) is used to retrieve data from Salesforce database objects. It is similar to SQL but specially designed for Salesforce.

It helps to:
- Retrieve records
- Filter data
- Sort results
- Access related object data

Example:

SELECT Name FROM Student__c

This retrieves all student names.

---

## 2. What is an Apex Trigger?

An Apex Trigger is code that runs automatically before or after changes happen to Salesforce records.

Triggers are used when records are:
- Inserted
- Updated
- Deleted
- Restored

Example:  
When a student registers, a welcome email is sent automatically.

---

## 3. Difference Between Flow and Trigger

| Flow | Trigger |
|------|---------|
| No coding required | Requires coding |
| Easy to build | More flexible |
| Used for simple automation | Used for complex logic |
| Admin friendly | Developer friendly |

### Use Flow For:
- Email notifications
- Updating simple records
- Approval process

### Use Trigger For:
- Complex validation
- Bulk processing
- Advanced automation
- External API calls

---

## 4. Difference Between Before and After Trigger

| Before Trigger | After Trigger |
|---------------|--------------|
| Runs before saving record | Runs after saving record |
| Used for validation | Used for related actions |
| Faster field modification | Used when record ID is needed |

Example:

**Before Insert:** Validate student age  
**After Insert:** Send welcome email

---

## 5. Trigger Use Cases (College Management System)

### Student Registration
**Event:** After Insert  
**Action:** Send welcome email

### Course Full
**Event:** After Update  
**Action:** Notify faculty

### Low Attendance
**Event:** After Update  
**Action:** Send warning to student

### Fee Payment Complete
**Event:** After Update  
**Action:** Generate receipt

### Result Published
**Event:** After Insert  
**Action:** Notify student

---

## 6. Query Examples

- Find all students in Course A
- Find all courses handled by Faculty X
- Find students with attendance below 75%
- Find students with pending fees
- Find students who passed all exams

---

## 7. Reflection

Enterprise systems react automatically to data changes because manual monitoring is slow and inefficient.

Automatic reactions help:
- Save time
- Reduce errors
- Improve consistency
- Provide instant response
- Increase system intelligence

Example:  
If attendance drops below 75%, the system immediately sends a warning message.

This makes enterprise systems faster and smarter.

---

## Reflective Questions

### Why do systems need triggers?
Triggers automate actions instantly after data changes.

### Difference between polling and event-driven systems?
Polling checks repeatedly for updates.  
Event-driven reacts instantly when an event happens.

### Why are database queries important?
They retrieve specific data quickly.

### When should Flows be preferred over Triggers?
For simple automation without coding.

### What problems happen if automation becomes too complex?
It becomes difficult to maintain and debug.

### Why should developers think carefully before automating?
Poor automation can cause duplicate actions and system issues.

---

## Learning Outcome

Today I learned:

- How SOQL retrieves data
- What Apex Triggers do
- Flow vs Trigger
- Before vs After Trigger
- How enterprise systems react automatically to events
