# 🚀 Salesforce Summer Program – Day 5: Apex Introduction


## 📚 What is Apex?

Apex is Salesforce’s server-side programming language used to build custom business logic that cannot be handled by declarative tools like Flow or Validation Rules.

It is used for:
- Backend logic
- Database operations
- Complex automation
- External integrations

---

## ⚙️ Why Salesforce Needs Apex

Salesforce provides:
- Flow Builder
- Validation Rules
- Process Automation
- Formula Fields

But these are not enough for:

- Complex business rules
- Large-scale data processing
- External API integration
- Advanced decision-making logic

👉 So Apex is required for flexibility and control.

---

## ⚖️ Declarative vs Programmatic Development

### Declarative (Clicks / No Code)
- Flow
- Validation Rules
- Reports

✔ Easy  
✔ Fast  
✔ Low maintenance  

---

### Programmatic (Code - Apex)
- Custom logic
- API integration
- Complex conditions
- Bulk processing

✔ Powerful  
✔ Scalable  
✔ Flexible  

---

## 🔄 Flow vs Apex

| Feature | Flow | Apex |
|--------|------|------|
| Type | No-code | Code |
| Complexity | Low | High |
| Flexibility | Limited | Very High |
| Use Case | Simple automation | Complex logic |

---

## 🏗️ College Management System (Integration Task)

### CRM Concept

Salesforce acts as a CRM for managing:

- Students
- Courses
- Faculty
- Admissions

---

### 🧩 Objects

**Student**
- Name
- Email
- Attendance
- GPA
- Fee Status

**Course**
- Course Name
- Total Seats
- Filled Seats

**Faculty**
- Name
- Department

---

### 🔗 Relationships

- Student ↔ Course (Many-to-Many)
- Faculty ↔ Course (One-to-Many)

---

### ✅ Validation Rules

- Email is required
- Attendance must be 0–100
- GPA must be valid range

---

### ⚡ Flow Usage

- Auto admission confirmation email
- Seat availability notification
- Registration success alerts

---

### 💡 Apex Usage

- Eligibility logic
- Fee calculation
- External integrations
- Complex business rules

---

## 💼 Real Examples Where Apex is Needed

### 1. Complex Fee Calculation
Includes:
- Scholarship rules
- Discounts
- Taxes
- Late fees

👉 Too complex for Flow

---

### 2. Payment Gateway Integration
- External API call
- Payment verification
- Record update

👉 Requires Apex

---

### 3. Advanced Eligibility Logic
Conditions:
- Attendance > 75%
- Fees paid
- GPA threshold
- Seat availability

👉 Multiple conditions → Apex required

---

## 🧠 Apex Thinking Exercise

### Flow is NOT enough when:

- External system integration is needed
- Complex calculations are involved
- Large datasets must be processed

👉 Apex is required for control and performance.

---

## 🧾 Pseudocode (Simple Logic)

IF seats = 0  
THEN block registration  

IF attendance < 75  
THEN send warning  

IF fee not paid  
THEN block exam entry  

IF GPA > 8  
THEN allow scholarship  

---

## ❓ Reflection Task

### Why can’t all enterprise logic be built using only clicks?

Because:
- Business rules are complex
- Systems must scale
- Integrations are required
- Performance matters
- Logic changes frequently

👉 Click-based tools are limited in flexibility.

---

## 🧠 Key Questions

### 1. Why is Apex needed if Salesforce already has Flows?
Because Flow cannot handle complex logic, integrations, and large-scale processing.

---

### 2. When should developers prefer no-code solutions?
When requirements are simple and easy to maintain.

---

### 3. What problems require custom programming?
- APIs
- Complex logic
- Bulk data processing
- Advanced automation

---

### 4. Why is business logic important?
It defines how the system behaves in real-world scenarios.

---

### 5. Why avoid unnecessary coding?
Because declarative tools are easier to maintain.

---

### 6. How does programming increase flexibility?
It allows complete control over system behavior.

---

