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

### Key System Models

- **ERD (Entity-Relationship Diagram)** for users, time slots, commitments, and chats  
- **Class Diagrams** outlining system components and metadata  
- **Use Case Diagrams** for major system interactions  
- **Wireframes** for Admin Dashboard, Sign-Up Screen, Mobile Schedule  
- **User Flows** for core scenarios (signup, admin oversight, slot swap)

## Security & Infrastructure

- Secure login using password encryption and token sessions  
- Role-based permissions (e.g., Admins can edit schedules, Users cannot)  
- QR/barcode scanning integrated into the check-in system (proposed)  
- System designed with GDPR, HIPAA, and FLSA awareness in mind  

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
