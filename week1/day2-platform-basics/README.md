# Day 2 – Salesforce Platform Basics

## What is Salesforce Platform?

Salesforce Platform is a cloud-based platform used to build CRM applications, automate business processes, store customer data, and develop scalable business solutions.

It provides:
- CRM services
- Cloud storage
- Automation tools
- Security
- App development tools

Salesforce uses a multi-tenant architecture where multiple organizations share the same infrastructure while keeping data secure and separated.

---

# CRM Concepts in Salesforce

CRM concepts are represented in Salesforce using Objects and Apps.

| CRM Concept | Salesforce Representation |
|---|---|
| Customer Company | Account Object |
| Customer Person | Contact Object |
| Sales Deal | Opportunity Object |
| Activities | Task/Event |

Example:
- Account stores company information
- Contact stores customer details
- Opportunity tracks sales deals

---

# What is an App in Salesforce?

An App in Salesforce is a collection of related objects, tabs, and functionalities designed for a specific business process.

### Example:
Sales App includes:
- Accounts
- Contacts
- Opportunities
- Reports

Apps help users access all related features from one place.

---

# What is an Object?

An Object is a database table used to store data in Salesforce.

Objects contain:
- Fields (columns)
- Records (rows)

## Types of Objects

### Standard Objects
Provided by Salesforce:
- Account
- Contact
- Opportunity

### Custom Objects
Created by users according to business needs.

### Example:
Student Object:
- Student Name
- Roll Number
- Department

---

# What is a Tab?

A Tab is used to access objects, records, dashboards, or apps in Salesforce.

Tabs help users navigate the platform easily.

### Example:
- Student Tab
- Faculty Tab
- Opportunity Tab

---

# Difference Between App and Object

| App | Object |
|---|---|
| Collection of related features | Stores data |
| Used for workflow management | Used for data management |
| Contains tabs and objects | Contains records and fields |
| Example: Sales App | Example: Contact Object |

---

# Multi-Tenant Architecture

Multi-tenant architecture means many organizations share the same Salesforce infrastructure while their data remains secure and isolated.

## Benefits
- Cost efficient
- Automatic updates
- Scalable
- Easy maintenance

---

# Configuration vs Coding

## Configuration (No Code)

Configuration means using built-in Salesforce tools without writing code.

### Used When
- Requirements are simple
- Standard functionality is enough
- Faster implementation is needed

### Examples
1. Creating validation rules
2. Building workflows using Flow Builder

### Advantages
- Fast development
- Easy maintenance
- No programming knowledge required

---

## Coding (Apex)

Coding means developing custom functionality using Apex, Lightning Components, APIs, or Visualforce.

### Used When
- Business logic is complex
- Custom integration is needed
- Advanced functionality is required

### Examples
1. Payment gateway integration
2. Complex approval logic

### Advantages
- High customization
- Advanced functionality support

---

# When Should We Use Configuration Instead of Code?

Use configuration when:
- Standard Salesforce features solve the problem
- Requirement is simple
- Faster deployment is needed
- Maintenance should be easy

Use coding when:
- Complex logic is involved
- Custom UI is required
- External system integration is needed

---

# How Salesforce Allows Developers to Extend Functionality

Salesforce allows developers to extend functionality using:
- Apex
- Lightning Web Components (LWC)
- APIs
- Triggers
- Visualforce Pages

Developers can:
- Build custom applications
- Automate business logic
- Integrate external systems
- Create custom UI components

---

# System Design Example

## App Name
College Management App

---

## Objects Inside the App

### Standard Objects
- Contact
- Task

### Custom Objects
1. Student
2. Faculty
3. Course
4. Attendance
5. Fees

---

# User Interaction

## Admin
- Manage students
- Assign courses
- Generate reports

## Faculty
- Mark attendance
- Upload marks

## Students
- View attendance
- Check fee status

Users interact through tabs, forms, reports, and dashboards.

---

# End of Day Learning Outcome

By completing Day 2:
- Learned Salesforce platform structure
- Understood Apps, Objects, and Tabs
- Learned CRM integration in Salesforce
- Understood configuration vs coding
- Learned how developers build on Salesforce platform


