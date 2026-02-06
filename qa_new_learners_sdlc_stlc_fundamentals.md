# QA New Learners Documentation

## 1. Introduction
This document is designed for **new QA learners** to understand the **software development lifecycle (SDLC)**, **software testing lifecycle (STLC)**, and the overall ecosystem in which QA operates. It explains *who does what*, *why QA is important*, and *how testing fits into real-world projects*.

---

## 2. Project Ecosystem Overview

### 2.1 Stakeholders

| Role | Description | Examples |
|---|---|---|
| **Client / Customer** | The organization that needs the software | HRM Client |
| **End Users** | People who use the application | Employees, HR users |
| **Development Company** | Builds and delivers the software | HCL, Wipro, Infosys |
| **Product Companies** | Own and maintain products | Apple, Microsoft, Meta |

### 2.2 Application Type
- **Web Application**
- Example: **HRM (Human Resource Management) System**

---

## 3. Stages of SDLC (Software Development Life Cycle)

SDLC defines **how a software product is planned, built, tested, deployed, and maintained**.

### 3.1 Requirement Collection
- **Handled by**: Business Analyst (BA) / Product Owner (PO)
- **Documents**:
  - BRD (Business Requirement Document)
  - FRD (Functional Requirement Document)
- **Outcome**: Clear understanding of *what needs to be built*

---

### 3.2 Design
- **Handled by**: UI/UX Engineers, Design Engineers
- **Artifacts**:
  - Wireframes
  - Mockups
  - Design specifications
- **Outcome**: How the application will *look and behave*

---

### 3.3 Coding / Development
- **Handled by**:
  - Frontend Developers
  - Backend Developers
  - Database Engineers
  - Full Stack Developers
- **Output**:
  - Application build
  - Unit-tested code
- **Environment**: Local / Dev environment

---

### 3.4 Testing
- **Handled by**: QA Team
- **Types**:
  - Functional Testing
  - Non-Functional Testing (Performance, Security, Usability)
- **Process Followed**: STLC
- **Outcome**: Quality-verified application

---

### 3.5 Deployment
- **Handled by**:
  - Developers
  - DevOps / Infrastructure Team
  - Release Engineers
- **Activities**:
  - Build deployment
  - Environment configuration
  - Production release

---

### 3.6 Maintenance & Support
- **Handled by**:
  - Developers
  - Support Teams (L1 / L2 / L3)
- **Activities**:
  - Bug fixes
  - Enhancements
  - Production support

---

## 4. STLC (Software Testing Life Cycle)

STLC defines **how testing activities are planned and executed**.

---

### 4.1 Requirement Analysis
- **Input**:
  - BRD / FRD
  - User Stories / PBIs (Jira, Azure Boards)
- **Type of Testing**: Static Testing
- **QA Activities**:
  - Requirement understanding
  - Identifying gaps
  - Asking clarifying questions

---

### 4.2 Test Design

#### a. Test Planning
- Test Plan
- Test Strategy

#### b. Test Scenario Design
- High-level test conditions

#### c. Test Case Design
- Detailed steps
- Expected results
- Test data preparation

#### d. RTM (Requirement Traceability Matrix)
- Maps requirements to test cases
- Ensures full test coverage

---

### 4.3 Test Environment Setup
- **Environment**: QA / Test server
- **Pre-requisites**:
  - Correct build deployed
  - Required access provided
  - Test data available

---

### 4.4 Test Execution
- **Execution Types**:
  - Manual Testing
  - Automation Testing
- **Activities**:
  - Execute test cases
  - Update test results
  - Log defects

---

### 4.5 Defect Reporting

A good defect should include:
- Defect Title
- Detailed Description
- Steps to Reproduce
- Expected vs Actual Result
- Severity (Impact)
- Priority (Urgency)
- Root Cause Analysis (RCA)

Tools: Jira, Azure Boards, Bugzilla

---

### 4.6 Test Sign-Off
- **Criteria**:
  - All critical test cases executed
  - No open high-severity defects
- **Deliverables**:
  - Test Execution Report
  - Bug Report
  - RTM
  - QA Sign-off

---

## 5. Key Takeaways for New QA Learners
- QA is involved **from requirement analysis to release sign-off**
- Understanding requirements is more important than tool knowledge
- Documentation is a **core QA responsibility**
- Quality is a **shared responsibility**, not only QA’s job

---

## 6. Next Learning Steps
- Manual Testing Fundamentals
- Test Case Writing Practice
- Jira / Azure Boards basics
- Basic SQL & API testing
- Automation basics (Selenium / REST Assured)

---

**End of Document**

