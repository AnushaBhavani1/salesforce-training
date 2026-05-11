# Salesforce Summer Program – Day 3
# Data Modeling, Formula Fields & Validation Rules

---

# 1. Difference Between App, Object, Record, Field

## App
An app is a collection of related tabs, objects, and tools designed for a specific business purpose.

**Example:**  
College Management App

---

## Object
An object is like a database table that stores similar business information.

**Example:**  
Student Object stores student details.

---

## Record
A record is one single row of data inside an object.

**Example:**

| Student ID | Name | Age |
|------------|------|-----|
| 101 | Anu | 20 |

---

## Field
A field stores one specific type of information.

Examples:

- Name
- Age
- Email
- Course

---

# 2. Standard vs Custom Objects

## Standard Objects
Prebuilt Salesforce objects.

Examples:

- Account
- Contact
- Lead
- Opportunity

Used for CRM processes.

---

## Custom Objects
Objects created by users for business-specific needs.

Examples:

- Student__c
- Faculty__c
- Course__c
- Department__c

Used when standard objects do not match business requirements.

---

# 3. College Data Model

## Objects

### Student
- Student ID
- First Name
- Last Name
- Email
- Age
- Course

### Faculty
- Faculty ID
- Name
- Email
- Department

### Course
- Course ID
- Course Name
- Total Seats
- Filled Seats

### Department
- Department ID
- Department Name
- Location

---

## Relationships

### Department → Faculty
One department has many faculty members.

Relationship Type: Lookup

Reason: Faculty can move to another department.

---

### Department → Course
One department offers many courses.

Relationship Type: Lookup

Reason: Courses can be reassigned.

---

### Course → Student
One course has many students.

Relationship Type: Lookup

Reason: Students can change courses.

---

## Data Model Diagram

```plaintext
Department
   |
   |---- Faculty
   |
   |---- Course
            |
            |---- Student
```

---

# 4. Formula Fields

Formula Fields calculate values automatically.

---

## Formula 1: Full Name

```plaintext
First_Name__c & " " & Last_Name__c
```

Why automatic?  
Prevents manual typing mistakes.

---

## Formula 2: Remaining Seats

```plaintext
Total_Seats__c - Filled_Seats__c
```

Why automatic?  
Shows live seat availability.

---

## Formula 3: Percentage

```plaintext
(Obtained_Marks__c / Total_Marks__c) * 100
```

Why automatic?  
Ensures accurate academic result calculation.

---

# 5. Validation Rules

Validation Rules prevent invalid data entry.

---

## Validation Rule 1: Email Cannot Be Empty

```plaintext
ISBLANK(Email__c)
```

Prevents: Missing communication details.

---

## Validation Rule 2: Student Age Cannot Be Negative

```plaintext
Age__c < 0
```

Prevents: Impossible student records.

---

## Validation Rule 3: Course Seats Cannot Exceed Limit

```plaintext
Filled_Seats__c > Total_Seats__c
```

Prevents: Overbooking students.

---

# 6. Reflection – Why Structured Enterprise Data Matters

Companies handle large amounts of data.

Random spreadsheets cause:

- Duplicate entries
- Manual errors
- Missing relationships
- Poor reporting
- Difficult maintenance

Structured enterprise data provides:

- Accuracy
- Better reporting
- Automation
- Security
- Easy maintenance
- Real-time updates

This is why companies use Salesforce instead of random spreadsheets.

---

# Reflective Questions

## 1. Why can’t companies manage everything using Excel sheets?

Excel becomes difficult when data grows large and relationships become complex.

---

## 2. Why are relationships important between objects?

They connect related data for reporting and automation.

---

## 3. What problems happen if data is inconsistent?

Wrong reports, duplicate records, and poor business decisions.

---

## 4. Why should repetitive calculations be automated?

Automation saves time and reduces human error.

---

## 5. Why should invalid data be blocked early?

It prevents future business problems.

---

## 6. Why is Salesforce called a metadata-driven platform?

Because Salesforce stores structure as metadata, allowing customization without changing core code.

---

# End of Day Outcome

After Day 3, I understand:

- How Salesforce stores business data
- How enterprise systems are structured
- Why relationships are critical
- Difference between Formula Fields and Validation Rules
- How no-code business logic works

---

**Day 3 Completed Successfully**
