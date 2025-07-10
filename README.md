# AdoraPlan System  
**Eucharistic Adoration Scheduler & System Design Case Study**

AdoraPlan is a complete system design and documentation project built to modernize the way Eucharistic Adoration is coordinated. Originally developed for the **St. Pius X Parish**, this scalable platform aims to enhance spiritual engagement, reduce administrative burden, and improve accessibility through a secure, role-based digital scheduling system. The project encompasses everything from feasibility analysis to system modeling and wireframes—laying the foundation for a full-stack implementation in the future.

---

## Project Purpose

Manual sign-up sheets for adoration scheduling are difficult to manage and prone to errors, particularly when continuous presence is required. This project proposes a digital solution to address these inefficiencies by building a structured and intuitive system that allows:

- Secure digital scheduling for parishioners  
- Administrative visibility and oversight  
- Clear user roles and workflows  
- Accessible and mobile-friendly interfaces

The system was originally scoped for **St. Pius X Parish** with future expansion potential to other parishes or the **Archdiocese of Seattle**.

---

## Objectives

- Replace manual adoration sign-up sheets with a digital platform  
- Allow parishioners to **reserve**, **manage**, **trade**, or **drop** time slots  
- Provide a **Q&A communication channel** between parishioners  
- Enforce **secure access** via barcode scans and encrypted login  
- Support parish staff with **reporting tools** and **schedule oversight**  
- Enhance spiritual participation through accessibility and dependability

---

## Deliverables

| Category             | Contents                                                                 |
|---------------------|--------------------------------------------------------------------------|
| **System Proposal** | Executive Summary, Feasibility Analysis, Requirements, Risk Assessment   |
| **Specification**   | Class Diagrams, Metadata, Architecture Design, Infrastructure Plan       |
| **Modeling**        | Use Case Diagrams, Sequence Diagrams, ERD                                |
| **Design**          | Wireframes (Mobile + Desktop), User Flows                                |
| **Documentation**   | README, Glossary, References, Appendices                                 |

---

## System Design Components

### Specification Document – Table of Contents

![Specification TOC](images/Screenshot%20(128).png)  
This table of contents outlines the full technical scope of the system. It includes key components such as infrastructure design, class definitions, metadata, data flow, and system requirements. It served as the anchor for detailed system modeling and made stakeholder alignment easier.

### Proposal Document – Table of Contents

![Proposal TOC](images/Screenshot%20(124).png)  
This document presents the strategic case for building AdoraPlan. It includes feasibility analysis, risk assessment, stakeholder goals, and initial technical decisions. It also scoped early non-functional requirements like accessibility for elderly users and GDPR compliance.

---

### Functional Scope

- Time slot management (sign-up, drop, swap)
- User authentication with role-based access (Admin, Parishioner, Guest)
- QR/barcode scan for attendance logging
- Notifications and reminders
- Weekly reporting for administrators
- Q&A Chat module for parishioner communication

### Non-Functional Requirements

- Accessible UX/UI for elderly users  
- Security (GDPR-compliant user data handling)  
- Mobile-responsiveness  
- Low-latency schedule interactions  
- Fault tolerance during high usage periods  

---

##  System Architecture

### High-Level Design

- **3-Tier Architecture:**
  - **Presentation Layer:** Figma wireframes, mobile-first design  
  - **Logic Layer:** Flow diagrams, sequence models (designed)  
  - **Data Layer:** Class diagrams, metadata model, simulated DB schema

### Architecture Overview

![Architecture Overview](images/Screenshot%20(131).png)  
A 3-tier model outlines how the system separates logic, data, and presentation concerns. The Presentation Layer includes responsive UIs; the Logic Layer models core scheduling behavior and rules; the Data Layer contains class-backed models tied to a simulated database schema.

---

### Key System Models

- **ERD (Entity-Relationship Diagram)** for users, time slots, commitments, and chats  
- **Class Diagrams** outlining system components and metadata

![Class Diagram](images/Screenshot%20(129).png)  
These diagrams define the object-oriented structure of the platform. Core classes include `User`, `TimeSlot`, `Commitment`, and `ChatThread`. Each class is annotated with attributes and basic methods, showing how entities relate across the data layer.

---

### Class Diagram Detail

![Class Diagram Detail](images/Screenshot%20(130).png)  
This close-up illustrates specific metadata fields (e.g., `Commitment.status`, `User.role`) that support dynamic behavior like schedule filtering, role-based permissions, and communication threads. The details help ensure the system can scale beyond St. Pius X to other parishes.

---
- **Use Case Diagrams** for major system interactions  
- **Wireframes** for Admin Dashboard, Sign-Up Screen, Mobile Schedule

### Navigation Flow Diagram

![Navigation Diagram](images/Screenshot%20(134).png)  
This user flow guides parishioners through the app from login → dashboard → slot management. It’s designed mobile-first with accessibility in mind, including minimal steps, large click areas, and contextual reminders. Admin navigation includes deeper layers for oversight and reporting.

---

- **User Flows** for core scenarios (signup, admin oversight, slot swap)

### Use Case Diagram

![Use Case Diagram](images/Screenshot%20(125).png)  
This UML diagram maps all major actors and their interactions with the system. Admins, parishioners, and guests each have distinct capabilities. This helped ensure user needs were clearly translated into actionable development features during early planning.

---

### Use Case Detail Example

![Use Case Detail](images/Screenshot%20(126).png)  
![Use Case Detail](images/Screenshot%20(127).png)  
This detail zooms into one specific use case—such as *“Swap Time Slot”*—showing preconditions (e.g., a slot must already be reserved), main flow (how a swap request is made), and alternate paths (e.g., if no one accepts the swap). It was key in preparing for system validation and error-handling.

---

## Security & Infrastructure

- Secure login using password encryption and token sessions
### Security Plan

![Security Diagram](images/Screenshot%20(133).png)  
The login and access control model secures the system using encrypted sessions and QR/barcode-based check-ins. Admins have broader control over user accounts, while regular users are limited to their own commitments. This diagram also references GDPR and HIPAA compliance areas.

---
- Role-based permissions (e.g., Admins can edit schedules, Users cannot)  
- QR/barcode scanning integrated into the check-in system (proposed)  
- System designed with GDPR, HIPAA, and FLSA awareness in mind

### Nodes & Deployment Diagram

![Deployment Diagram](images/Screenshot%20(132).png)  
This shows how the system components can be hosted and scaled—e.g., using Firebase Auth for login, Firestore or PostgreSQL for DB, and a Django REST API or serverless backend. It includes considerations for artifacts like static reports, cloud functions, and failover handling.

---

## What I Learned

### Requirement Gathering
- Conducted stakeholder interviews and interpreted community needs into structured, formal requirements  
- Balanced spiritual mission with technical feasibility and user constraints  

### System Modeling
- Created use case and class diagrams using UML tools like LucidChart  
- Defined metadata models, ERDs, and relationships between users, time slots, and commitments  

### Technical & Lifecycle Planning
- Understood full project phases from proposal to architecture  
- Analyzed feasibility and estimated costs based on technical and human resources  

### Security & Accessibility
- Researched secure login practices and compliant data handling for church-related use cases  
- Designed interfaces accessible to elderly parishioners through larger UI elements and minimal interaction steps  

### Testing & Maintenance
- Designed a long-term maintenance and stability roadmap  
- Drafted a testing plan focused on usability, reliability, and failover conditions  

---

## Future Improvements

- **Backend Implementation:** Convert wireframes and flows into a working MVP using Django or Firebase  
- **Mobile App Development:** Launch a PWA or native app version for on-the-go scheduling and reminders  
- **Slot Swap Logic:** Implement intelligent slot matching or swap recommendations to prevent unattended hours  
- **Admin Analytics Dashboard:** Add weekly summary reports on attendance, missed slots, and backup coverage needs  
- **Integration with Parish Systems:** Connect to Google Calendar, Flocknote, or Archdiocesan event platforms for unified coordination  
