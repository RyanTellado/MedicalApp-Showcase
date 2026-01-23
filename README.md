# Mobile Clinic Operations Platform  
### Distributed Health Records + Logistics System for Field Clinics (India & South Sudan)



![Impact](https://img.shields.io/badge/Impact-500k%2B%20Patients%20Served-blue)&nbsp;&nbsp;&nbsp;
![Role](https://img.shields.io/badge/Role-Project%20Lead-green)&nbsp;&nbsp;&nbsp;
![Status](https://img.shields.io/badge/Status-Field%20Deployed-success)

📌 Project Overview

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

## 📱 Interactive Product Showcase

### 1. Clinical History Retrieval & Visit Timeline  
The system retrieves a patient’s longitudinal record via a unique Aadhaar ID (SSN). Clinicians can instantly view prior visits and trends (e.g., weight, blood pressure, blood sugar, past prescription), supporting continuity of care across rotating mobile clinics.

| Interactive ID Search & History Retrieval | Clinical Assessment Entry |
| :---: | :---: |
| <img src="./id-entering-patient-history-ezgif.com-optimize.gif" width="320"> | <img src="./visit-history-ui-2.png" width="320"> |
| **Fast Lookup:** Instant query over a NoSQL longitudinal record. | **Visit Timeline:** Demo patient (John Doe) showing historical trends. |

---

### 2. Real-Time Medication Logic & Cloud Sync  
This section demonstrates the core automation layer. As clinicians enter vitals and prescriptions, backend logic performs calculations and synchronizes updates to the cloud database.

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

## 🧪 Development Process: From Prototype to Field System  
The first prototype failed in practice due to a mismatch between feature complexity and staff digital literacy. I spent months working directly with doctors, drivers, and administrators to observe real workflows, simplify interfaces, and move complexity into invisible backend automation. Features like clinic session activation, inventory deduction, and analytics export were added iteratively in response to operational breakdowns in the field. The system evolved through continuous testing, deployment, and redesign—driven by usability failures rather than abstract technical ambition.

---

## 🚀 Key Technical Innovations  
- **Clinic Session Orchestration:** Daily activation workflow binds doctors, support staff, drivers, vehicles, and geographic clusters into a single persistent session. Patient visits automatically associate with this session for consistent attribution and auditability.  
- **Automated Workflow Logic:** Java-based automation handles staff clock-ins and location assignments based on the first and last patient interactions of the day.  
- **Smart Inventory Intelligence:** Stock levels for medicines (e.g., Cipro-500, Amoxipen) deduct in real time as treatments are recorded, triggering low-stock flags for administrators.  
- **Offline-Tolerant Data Persistence:** Built on a NoSQL Firestore backend with workflows resilient to intermittent connectivity.  
- **Administrative Analytics Export:** Custom transformation layer exports nested NoSQL structures into organized Google Sheets for high-level operational analysis.

---

## 🛠️ Technical Stack  
- **Frontend:** Android Studio (Java)  
- **Backend & Database:** Firebase Cloud Firestore  
- **Deployments:** India (Parivaar, Samaritain Help Mission), South Sudan (SuDRO)

<details>
<summary><b>📖 Project Backstory (Condensed)</b></summary>

When I first connected with a rural clinic network in India, most patient history lived in paper logs—hard to search, easy to lose, and impossible to aggregate across visits. My first version of this system technically worked but failed in practice due to digital literacy barriers. The project only became viable after sustained field iteration: simplifying UX, automating logistics invisibly, and redesigning workflows around how staff actually operated. What started as a technical experiment became a production system through testing, failure, and continuous adaptation.

</details>
