# Day 4 - Flow Builder

## What is Flow Builder?

Flow Builder is Salesforce’s no-code automation tool used to automate business processes without writing code.

It helps businesses create workflows using drag-and-drop components to automate tasks such as:

- Creating records
- Updating records
- Sending notifications
- Collecting user input
- Running approval processes
- Connecting business systems

Flow Builder improves speed, consistency, and efficiency in enterprise software.

---

# Why Automation Matters

Automation reduces repetitive manual work and improves operational efficiency.

Benefits:

- Saves time
- Reduces human errors
- Improves productivity
- Ensures process consistency
- Speeds up execution
- Reduces operational cost

In enterprise systems, automation helps organizations handle large-scale repetitive tasks efficiently.

---

# Types of Flows

| Flow Type | Trigger | Example |
|-----------|---------|---------|
| Screen Flow | User action | Student registration form |
| Record-Triggered Flow | Record create/update/delete | Auto confirmation email |
| Scheduled Flow | Time/date | Monthly fee reminders |
| Autolaunched Flow | Called automatically | Update course data |
| Platform Event Flow | External event | Payment success updates record |
| Record-Triggered Orchestration Flow | Record change starts multi-step process | Student admission approval |

---

# Screen Flow

Screen Flow is an interactive flow that displays screens to users and collects input.

### Features

- Requires user interaction
- Collects data through forms
- Guides users step-by-step

### Example

Student Registration Process

Student enters:

- Name
- Email
- Course selection

System processes submission and confirms registration.

### Use Cases

- Registration forms
- Surveys
- Guided onboarding
- Data collection

---

# Record-Triggered Flow

Record-Triggered Flow runs automatically when a record is created, updated, or deleted.

### Features

- No user interaction
- Executes in background
- Real-time automation

### Example

When a student registration record is created:

- Generate student ID
- Send confirmation email
- Update seat count

### Use Cases

- Notifications
- Record updates
- Automatic processing

---

# Other Important Flow Types

## Scheduled Flow

Runs automatically at specific times.

Example:

Send monthly fee reminders.

---

## Autolaunched Flow

Runs automatically without screens.

Example:

Update student status automatically.

---

## Platform Event Flow

Runs when Salesforce receives an external event.

Example:

Payment gateway sends successful payment event.

Salesforce updates fee status.

---

## Record-Triggered Orchestration Flow

Manages multi-step business processes involving multiple users or approvals.

Example:

Admission request  
→ Document verification  
→ Faculty approval  
→ Fee confirmation  
→ Admission completion

---

# Automation Ideas (College Management System)

## 1. Auto Email After Registration

When a student registers, confirmation email is sent automatically.

### Benefit

- Instant response
- Better communication
- Saves admin effort

---

## 2. Auto Update Remaining Seats

When student joins course, available seats decrease automatically.

### Benefit

- Prevents overbooking
- Real-time seat tracking

---

## 3. Notify Faculty When Course is Full

Faculty gets notified when maximum capacity is reached.

### Benefit

- Helps batch planning
- Better course management

---

## 4. Generate Student ID Automatically

System generates unique student IDs.

Example:

STU2026001

### Benefit

- Avoids duplicates
- Organized records

---

## 5. Send Fee Payment Reminder

System reminds students before due date.

### Benefit

- Reduces late payments
- Improves fee collection

---

# Flow Diagram

## Automation Process: Auto Email After Registration

```plaintext
TRIGGER
Student submits registration form
        ↓
Get Student Details
        ↓
Decision:
Registration Successful?
    /         \
 YES          NO
 ↓             ↓
Generate ID   Show Error
 ↓
Send Confirmation Email
 ↓
Update Seat Count
 ↓
Update Student Record
 ↓
FINAL ACTION
Registration Completed
```

(Add flow-diagram.png in repository)

---

# Manual vs Automated Process

## Process: Fee Payment Reminder

# Manual Process

Admin:

- Checks fee due records
- Identifies pending students
- Sends reminder emails manually
- Tracks responses manually

### Problems

- Time consuming
- Errors possible
- Delays occur
- Students may be missed

---

# Automated Process

Salesforce automatically:

- Checks due dates
- Finds pending students
- Sends reminders
- Updates payment status

### Benefits

- Fast execution
- Accurate reminders
- No missed students
- Reduced admin workload

---

# Reflection: Why Automation Matters in Enterprise Systems

Automation is critical because enterprise systems process huge amounts of repetitive tasks.

Automation helps by:

- Improving speed
- Reducing manual effort
- Improving consistency
- Increasing productivity
- Lowering operational cost
- Improving customer experience

It allows employees to focus on strategic tasks instead of repetitive work.

---

# Reflective Questions

## 1. Why do companies automate workflows?

Companies automate workflows to improve efficiency, reduce errors, save time, and scale business operations.

---

## 2. What problems happen with manual processes?

Manual processes create delays, inconsistency, human errors, and increased workload.

---

## 3. Difference between Screen Flow and Record-Triggered Flow?

**Screen Flow**

Requires user interaction through forms or screens.

**Record-Triggered Flow**

Runs automatically when data changes.

---

## 4. Why is no-code automation powerful?

It allows business users to automate workflows without technical coding knowledge.

---

## 5. When should automation be avoided?

Automation should be avoided when:

- Human judgment is required
- Processes are unclear
- Business rules change frequently
- Sensitive approval decisions are involved

---

## 6. How does automation improve consistency and productivity?

Automation performs tasks the same way every time and removes repetitive manual work, improving consistency and allowing employees to focus on important work.

---

# End of Day Outcome

After completing Day 4, I clearly understand:

- How Salesforce automates workflows
- Why business process automation matters
- Types of Salesforce Flows
- Difference between manual and automated systems
- How no-code automation works in enterprise software
- How businesses improve productivity using automation
