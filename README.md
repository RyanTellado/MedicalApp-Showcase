# Humanitarian Medical Informatics System
### A "MyChart" for Rural Healthcare: Serving 500k+ Patients in India & South Sudan

![Impact](https://img.shields.io/badge/Impact-500k%2B%20Patients-blue)
![Role](https://img.shields.io/badge/Role-Project%20Lead-green)

## 📌 Project Overview
This platform serves as the digital backbone for humanitarian organizations (Parivaar, SuDRO) operating mobile hospitals. Much like **Epic or MyChart** in the U.S., this system provides a comprehensive "Patient Portal" for clinicians, transforming millions of paper-based tally marks into a searchable, longitudinal medical record.

* **Scale:** Replacing paper records for 500,000+ patients annually across 17+ districts.
* **Mission:** Bridging the digital literacy gap for field staff while ensuring data integrity in "dead zones" without internet.

---

## 📱 The Interface in Action
| Longitudinal Patient History | Administrative & Staff Automation |
| :--- | :--- |
| ![Assessment](./visit-history-ui.png) | *[Insert Workflow GIF Here]* |
| **Real-time Vitals:** Pulls historical trends (Weight, BP, Sugar) to ensure continuity of care. | **"Invisible" Logic:** Auto-logs staff hours and inventory based on mobile clinic activity. |

---

## 🚀 Key Technical Innovations

### 1. Longitudinal Care Engine
Unlike paper records that only capture a single visit, this Java-based engine uses Aadhar (ID) numbers to pull a patient's entire medical narrative. It alerts doctors to historical trends in weight and blood sugar, preventing critical oversights in rural treatment.

### 2. "Invisible" Workflow Automation
To accommodate users with limited digital literacy, I developed custom automation to handle administrative overhead silently:
* **Attendance Intelligence:** Automatically clocks staff in/out and assigns them to specific mobile clinics based on the first and last patient entries of the day.
* **Smart Inventory Management:** Real-time medicine tracking that deducts stock levels (e.g., ITRIM 200, Almox-500) automatically as treatments are recorded.

### 3. Resilient Data Architecture
Designed for the most remote areas of South Sudan and India, the app uses an offline-first architecture. All medical data persists locally using Java logic and automatically synchronizes with **Firebase Cloud Firestore** the moment connectivity is restored.

---

## 🛠️ Technical Profile
* **Frontend:** Android Studio (Java)
* **Backend & Database:** Firebase Cloud Firestore
* **Analytics:** Automated data transformation for export into Google Sheets for high-level organizational analysis.

<details>
<summary><b>📖 Read the Project Backstory (The "Why")</b></summary>

When I first connected with Parivaar, I found that each "tally mark" on paper was a person reduced by the limits of physical records. As a freshman at Stanford, I taught myself Android Studio to build a solution that preserves patient dignity and ensures life-saving longitudinal care.
</details>
