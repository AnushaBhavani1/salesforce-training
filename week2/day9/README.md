# Day 9 – LWC Communication & Architecture



# 📌 Component Communication in LWC

Lightning Web Components communicate to exchange data and trigger actions between components.

## Types of Communication

### 1. Parent → Child Communication
- Uses `@api`
- Parent component passes data to child component

### Example
Dashboard component sends student details to profile component.

---

### 2. Child → Parent Communication
- Uses Custom Events
- Child component sends events back to parent

### Example
Attendance component updates dashboard after attendance submission.

---

### 3. Communication Between Unrelated Components
- Uses Pub/Sub or Lightning Message Service (LMS)
- Enables communication between independent modules

---

# 📌 Dashboard Architecture

## 🎓 Student Dashboard
### Components
- Student Profile
- Attendance
- Courses
- Notifications

### Communication Flow
- Profile component sends student data
- Attendance component fetches records
- Notification component updates alerts

---

## 👨‍🏫 Faculty Dashboard
### Components
- Course Management
- Attendance Update
- Student Performance

### Communication Flow
- Faculty updates attendance
- Dashboard refreshes dynamically

---

## 👨‍💼 Admin Dashboard
### Components
- User Management
- Reports
- System Monitoring

### Communication Flow
- Admin actions trigger updates across modules

---

# 📌 Data Flow Explanation

## Example: Student Registration Process

### Step 1 – UI
Student fills registration form.

### Step 2 – Validation
Frontend validates:
- Required fields
- Email format
- Duplicate entries

### Step 3 – Flow
Validated data is sent to Apex Controller.

### Step 4 – Apex Logic
Apex processes business logic and inserts records.

### Step 5 – Database
Data is stored in Salesforce objects.

### Step 6 – Notification
System sends success message or email notification.

---

# 📌 Aura vs LWC

| Feature | Aura Components | Lightning Web Components |
|----------|----------------|--------------------------|
| Framework | Proprietary | Modern Web Standards |
| Performance | Slower | Faster |
| Architecture | Complex | Lightweight |
| Learning Curve | Difficult | Easier |
| JavaScript Support | Older Model | ES6+ Modern JS |
| Reusability | Moderate | High |

---

# 📌 Why Salesforce Moved from Aura to LWC

- Better performance
- Faster rendering
- Modern JavaScript standards
- Improved scalability
- Cleaner architecture
- Better developer experience

---

# 📌 Reflection

## Why Enterprise Applications Need Modular Architecture

Modular architecture helps:
- Improve maintainability
- Increase scalability
- Reduce code duplication
- Simplify debugging
- Enable reusable components
- Support team collaboration

Large enterprise applications become easier to manage when modules communicate independently.

---

# 📌 Revision Questions & Answers

## 1. Why do components communicate?
To exchange data and coordinate application behavior.

## 2. Difference between parent-child communication and events?
- Parent-child communication sends data downward.
- Events send information upward.

## 3. Why is modular architecture useful?
It improves scalability, maintenance, and reusability.

## 4. Why did Salesforce move toward LWC?
For better performance, modern standards, and cleaner architecture.

## 5. What problems happen in tightly coupled systems?
- Difficult maintenance
- Poor scalability
- Hard debugging

## 6. Why is frontend architecture important?
It improves user experience and application organization.

## 7. Why should UI and backend remain separate?
To allow independent development and flexibility.

## 8. Why do large systems need reusable modules?
To reduce repeated code and improve development speed.

---

