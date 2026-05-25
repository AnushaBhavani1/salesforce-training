# Salesforce Summer Program - Day 8

# Lightning Web Components (LWC) Basics

## Objective

The objective of Day 8 is to understand Lightning Web Components (LWC), component-based architecture, frontend vs backend development, reusable UI design, and the fundamentals of modern Salesforce user interface development.

---

# What is Lightning Web Components (LWC)?

Lightning Web Components (LWC) is Salesforce's modern framework for building user interfaces on the Salesforce platform.

LWC is based on standard web technologies:

- HTML
- JavaScript
- CSS
- Web Components
- ES6+ JavaScript

It allows developers to create reusable and independent UI components that can be combined to build scalable enterprise applications.

Instead of building an entire application as a single large page, LWC encourages breaking the application into small reusable components.

### Example

A Student Dashboard can be divided into:

- Header Component
- Student Information Component
- Attendance Component
- Fee Details Component
- Notification Component

Each component can be developed and maintained independently.

---

# Evolution of Salesforce UI Technologies

## 1. Visualforce

Visualforce was Salesforce's first UI technology.

### Features

- Server-side rendering
- Uses Apex Controllers
- Traditional page-based architecture

### Limitations

- Slower performance
- Less interactive user experience
- Difficult to build dynamic applications

---

## 2. Aura Components

Aura was introduced to provide a component-based development model.

### Features

- Component-based architecture
- Event-driven communication
- Client-side rendering
- Better user interaction

### Advantages

- Reusable components
- Dynamic applications
- Improved UI capabilities

### Limitations

- Complex architecture
- More files and boilerplate code
- Proprietary Salesforce framework
- Lower performance compared to LWC

---

## 3. Lightning Web Components (LWC)

LWC is Salesforce's latest UI framework.

### Features

- Based on web standards
- Faster rendering
- Lightweight architecture
- Better maintainability
- Improved security
- Modern JavaScript support

---

# Why Salesforce Moved from Aura to LWC

Salesforce introduced LWC to overcome the limitations of Aura and align development with modern web standards.

## 1. Better Performance

LWC uses native browser capabilities.

Benefits:

- Faster page loading
- Faster rendering
- Better responsiveness
- Reduced memory consumption

---

## 2. Standard Web Technologies

Aura relies on Salesforce-specific syntax.

LWC uses:

- HTML
- CSS
- JavaScript
- Web Components

Developers with web development knowledge can easily learn and work with LWC.

---

## 3. Less Code

Aura generally requires:

- Component
- Controller
- Helper
- Renderer
- Design File

LWC generally requires only:

- HTML
- JavaScript
- Meta XML

Result:

- Cleaner code
- Faster development
- Easier maintenance

---

## 4. Better Maintainability

LWC promotes modular design.

Advantages:

- Easy debugging
- Easy enhancements
- Easier testing
- Better code organization

---

## 5. Future-Proof Development

Salesforce recommends LWC for all new development projects.

LWC aligns with modern frameworks such as:

- React
- Angular
- Vue

---

# Aura vs LWC Comparison

| Feature | Aura | LWC |
|----------|----------|----------|
| Framework Type | Salesforce Specific | Standard Web Components |
| Performance | Moderate | High |
| Learning Curve | Complex | Easy |
| JavaScript Support | Limited | ES6+ |
| Browser Optimization | Framework Dependent | Native Browser Support |
| Code Complexity | High | Low |
| Development Speed | Slower | Faster |
| Maintenance | Difficult | Easier |
| Security | Lightning Locker | Lightning Web Security |
| Future Development | Supported | Preferred Framework |

---

# Aura Component Structure

### Aura Component

```html
<aura:component>
    <aura:attribute name="studentName" type="String"/>

    <lightning:card title="Student">
        {!v.studentName}
    </lightning:card>
</aura:component>
```

### Aura Controller

```javascript
({
    doInit : function(component,event,helper)
    {

    }
})
```

### Aura Helper

```javascript
({
    helperMethod : function(component)
    {

    }
})
```

Aura development generally requires multiple supporting files.

---

# Lightning Web Component Structure

Every LWC consists of three primary files.

## HTML File

```html
<template>
    <lightning-card title="Student">
        {studentName}
    </lightning-card>
</template>
```

## JavaScript File

```javascript
import { LightningElement } from 'lwc';

export default class Student extends LightningElement {

    studentName = 'Anu';

}
```

## Meta XML File

```xml
<?xml version="1.0" encoding="UTF-8"?>

<LightningComponentBundle
xmlns="http://soap.sforce.com/2006/04/metadata">

    <apiVersion>65.0</apiVersion>

    <isExposed>true</isExposed>

    <targets>
        <target>lightning__AppPage</target>
    </targets>

</LightningComponentBundle>
```

---

# Core Concepts of LWC

## Components

A component is a reusable and independent UI building block.

Examples:

- Login Form
- Header
- Attendance Widget
- Student Card
- Notification Panel

Benefits:

- Reusability
- Scalability
- Maintainability

---

## Template

The HTML file defines the user interface structure.

Example:

```html
<template>
    <h1>Welcome Student</h1>
</template>
```

---

## JavaScript Controller

Handles:

- Data
- Events
- Logic
- Apex Calls

Example:

```javascript
message = 'Welcome to Salesforce';
```

---

## Metadata Configuration

Meta XML controls:

- Component visibility
- Page availability
- Deployment settings

---

## Data Binding

Used to display dynamic data in UI.

Example:

```html
<template>
    {studentName}
</template>
```

```javascript
studentName = 'Anusha';
```

Output:

```
Anusha
```

---

## Event Handling

Used to respond to user actions.

Example:

```html
<lightning-button
label="Submit"
onclick={handleClick}>
</lightning-button>
```

```javascript
handleClick() {
    alert('Submitted');
}
```

---

# UI Thinking Exercise

## College Management System Screens

### 1. Student Registration Screen

Functions:

- Add Student
- Edit Student Information
- Upload Documents

---

### 2. Student Dashboard

Functions:

- Student Profile
- Academic Details
- Attendance Summary

---

### 3. Attendance Screen

Functions:

- View Attendance
- Attendance Reports

---

### 4. Faculty Dashboard

Functions:

- Manage Students
- Manage Courses
- Upload Marks

---

### 5. Notification Center

Functions:

- Announcements
- Alerts
- Event Notifications

---

# Component Breakdown

## Student Dashboard

### Header Component

Displays:

- Logo
- Navigation Menu

### Student Profile Component

Displays:

- Name
- Roll Number
- Department

### Attendance Component

Displays:

- Attendance Percentage
- Attendance Status

### Fee Details Component

Displays:

- Total Fee
- Paid Fee
- Remaining Balance

### Notification Component

Displays:

- Announcements
- Reminders
- Alerts

---

# Why Reusable Components are Useful

Reusable components provide:

## Faster Development

Develop once and reuse multiple times.

## Better Consistency

Maintains a uniform UI across applications.

## Easy Maintenance

Changes made once are reflected everywhere.

## Reduced Code Duplication

Less repeated code means fewer bugs.

## Improved Scalability

Applications become easier to expand.

---

# Frontend vs Backend Thinking

## Frontend Responsibilities

Frontend is responsible for user interaction.

Examples:

- Forms
- Buttons
- Navigation
- Notifications
- User Input

### Example

User clicks a Submit button.

Frontend captures the click event and sends a request.

---

## Backend Responsibilities

Backend handles business logic and data processing.

Examples:

- Database Operations
- Calculations
- Security Checks
- Validation Rules
- Data Retrieval

### Example

Backend validates student information and stores records in Salesforce.

---

# Secure Server-Side Development

Security is critical in enterprise applications because they store sensitive business data.

## Authentication

Verifies user identity.

Examples:

- Username
- Password
- Multi-Factor Authentication (MFA)

---

## Authorization

Controls what users can access.

Examples:

- Student Access
- Faculty Access
- Administrator Access

---

## Data Protection

Protects confidential information.

Examples:

- Student Records
- Financial Data
- Academic Information

---

## Input Validation

Prevents malicious or invalid data from entering the system.

Examples:

- SQL Injection Prevention
- Data Validation Rules
- Input Sanitization

---

# Reflection

## Why do modern enterprise systems use component-based UI architecture?

Modern enterprise systems use component-based architecture because:

1. Components are reusable.
2. Development becomes faster.
3. Maintenance becomes easier.
4. Applications become scalable.
5. Teams can work independently.
6. Code becomes modular and organized.
7. Testing becomes easier.
8. User interfaces remain consistent.
9. Development costs are reduced.
10. Overall software quality improves.

Component-based architecture is widely used in modern frameworks such as Salesforce LWC, React, Angular, and Vue.

---

# Interview Questions and Answers

## What is LWC?

LWC is Salesforce's modern component-based framework built using HTML, JavaScript, CSS, and Web Components to create fast and reusable user interfaces.

---

## Why did Salesforce introduce LWC?

Salesforce introduced LWC to improve performance, simplify development, leverage modern web standards, and provide a better user experience.

---

## Why is LWC better than Aura?

LWC provides better performance, cleaner code, modern JavaScript support, native browser capabilities, easier maintenance, and improved scalability compared to Aura.

---

## What are the main files in an LWC?

1. HTML File
2. JavaScript File
3. Meta XML File

---

## What is a reusable component?

A reusable component is a UI element that can be used multiple times across different pages without rewriting code.

---

## Difference between Frontend and Backend?

Frontend handles user interaction and presentation, while Backend manages business logic, security, processing, and database operations.

---

## Why should UI and Business Logic be separated?

Separating UI and business logic improves maintainability, security, scalability, testing, and code reusability.

---

=
LWC represents Salesforce's modern approach to building scalable, maintainable, secure, and high-performance enterprise applications.
