# Mobile Clinic Operations Platform  
### Distributed Health Records + Logistics System for Field Clinics (India & South Sudan)



![Impact](https://img.shields.io/badge/Impact-500k%2B%20Patients%20Served-blue)&nbsp;&nbsp;&nbsp;
![Role](https://img.shields.io/badge/Role-Project%20Lead-green)&nbsp;&nbsp;&nbsp;
![Status](https://img.shields.io/badge/Status-Field%20Deployed-success)

## Project Overview

This platform is a MyChart-style mobile app and backend system built for humanitarian healthcare organizations operating mobile clinics in India and South Sudan (including Parivaar, Samaritain Help Mission, and SuDRO Sudan).

It replaces paper-based workflows (tally marks and handwritten logs) with a digital system that supports both patient care and clinic operations.

At a high level, the platform consists of:
- a **Clinician App** for visit documentation and longitudinal patient history  
- an **Admin App** for inventory management, staff coordination, and multi-district operations  

In practice, it functions like a lightweight EHR + logistics layer for field clinics, designed to work offline on low-cost Android devices and to be usable by non-technical staff.

I designed and built both the Android application and the backend system, including automation for inventory updates, clinic logistics, and analytics export in google sheets

**Impact:** 500,000+ patients served annually  
**Active Clinics:** 50+ mobile clinics  
**Design Constraints:** intermittent connectivity, limited digital literacy, low-cost Android devices  

This project proves I can build a system that ran in real clinics with non-technical users and scaled across districts with real operational consequences.


---

## Interactive Product Showcase

### 1. Clinical History Retrieval & Visit Timeline  
The system retrieves a patient’s longitudinal record via a unique Aadhaar ID (SSN). Clinicians can instantly view prior visits and trends (e.g., weight, blood pressure, blood sugar, past prescription), supporting continuity of care across rotating mobile clinics.

| Interactive ID Search & History Retrieval | Clinical Assessment Entry |
| :---: | :---: |
| <img src="./id-entering-patient-history-ezgif.com-optimize.gif" width="320"> | <img src="./visit-history-ui-2.png" width="320"> |
| **Fast Lookup:** Instant query over a NoSQL longitudinal record. | **Visit Timeline:** Demo patient (John Doe) showing historical trends. |

---

### 2. Real-Time Automation Logic & Cloud Sync

This section demonstrates the core automation layer. As clinicians enter vitals and prescriptions, backend logic performs dosage calculations, updates medicine inventory, and synchronizes changes to the cloud database in real time.  

The same automation layer also updates the active clinic assignment and logs staff activity as patients are seen.

| Real-Time Database Synchronization |
| :---: |
| <img src="./patient-diagnosis-medicine-calculation.gif" width="900"> |
| **Split-Screen Proof:** The backend updates medicine quantities (e.g., *Amycordial*) immediately as the assessment form is processed. |

---

### 3. Clinic Operations & Staff Automation

This layer handles the real-world operations of mobile healthcare delivery: inventory management, daily clinic activation, staff coordination, and payroll-relevant activity tracking. It replaces manual staff logs and paper inventory sheets with automation that assigns clinic teams, tracks usage, and synchronizes operational data across districts.

| Smart Inventory Management | Daily Clinic Activation & Staff Assignment |
| :---: | :---: |
| <img src="./medicine-inventory-ui.png" height="540"> | <img src="./daily-activation-staff-assignment-ezgif.com-video-to-gif-converter.gif" height="540"> |
| **Inventory Tracking:** Real-time stock levels for critical medicines (e.g., Cipro-500, Amoxipen) with automatic deductions as treatments are recorded. Administrators can also manually restock inventory by logging new shipments directly into the system. | **Staff Orchestration:** Doctors, attendants, drivers, and vehicles are **automatically assigned** to a mobile clinic at the start of the day and bundled into a single **clinic session**. All patient visits and vehicle activity are **logged against this session** for daily coordination and accountability.



---

## Development Process: From Prototype to Field System  
The first prototype failed in practice due to a mismatch between feature complexity and staff digital literacy. I spent months working directly with doctors, drivers, and administrators to observe real workflows, simplify interfaces, and move complexity into invisible backend automation. Features like clinic session activation, inventory deduction, and analytics export were added iteratively in response to operational breakdowns in the field. The system evolved through continuous testing, deployment, and redesign—driven by usability failures rather than abstract technical ambition.

## Development Process: From Prototype to Field System

The first version of the app failed in practice because it was too complex for clinic staff to use reliably. I spent months working directly with doctors, drivers, and administrators to observe real workflows, simplify the interface, and move complexity into backend automation.

Features like daily clinic activation, automatic inventory deduction, and analytics export were added iteratively in response to real breakdowns in the field. The system evolved through continuous testing, deployment, and redesign—driven by usability failures rather than abstract technical goals.

---

## Key Technical Innovations

- **Daily Clinic Session Automation:** Each clinic day is activated as a single session that binds doctors, attendants, drivers, vehicles, and villages together. All patient visits automatically attach to this session for consistent tracking and auditability.

- **Activity-Based Time Tracking:** Staff are automatically clocked in with the first patient visit and clocked out with the last, eliminating manual attendance logs and enabling payroll automation.

- **Real-Time Inventory Automation:** Medicine stock levels (e.g., Cipro-500, Amoxipen) deduct automatically as treatments are recorded, with low-stock alerts triggered for administrators.

- **Offline-Resilient Sync:** Data is stored locally and synchronized to the cloud when connectivity becomes available, enabling reliable operation in low-signal environments.

- **Operations Analytics Export:** Clinic and patient data is automatically transformed into structured Google Sheets for high-level operational analysis and reporting.

---

## Technical Stack

- **Mobile App:** Android (Java), XML-based UI  
- **Backend & Database:** Firebase Cloud Firestore  
- **Sync Model:** Offline-first with automatic cloud synchronization  
- **Analytics Export:** Google Sheets integration  
- **Deployment Regions:** India and South Sudan
