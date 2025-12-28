# Humanitarian Medical Informatics System
### A "MyChart" for Rural Healthcare: Serving 500k+ Patients in India & South Sudan

![Impact](https://img.shields.io/badge/Impact-500k%2B%20Patients-blue)
![Role](https://img.shields.io/badge/Role-Project%20Lead-green)

## 📌 Project Overview
This platform serves as the digital backbone for humanitarian organizations (Parivaar, Samaritain Help Mission, SuDRO Sudan) operating mobile hospitals. Much like **Epic or MyChart** in the U.S., this system provides a comprehensive "Patient Portal" for clinicians and "Admin Portal" for administrative staff, replacing their paper-based system which used tally marks into a searchable, longitudinal medical record.

* **Scale:** Replacing paper records for 500,000+ patients annually across 17+ districts.
* **Mission:** Bridging the digital literacy gap for field staff while ensuring data integrity in "dead zones" without internet.

---

## 📱 Product Showcase

### 1. Clinical Assessment & History
This system provides a comprehensive EMR (Electronic Medical Record) interface, retrieving a patient's medical narrative using unique IDs. Doctors can instantly view historical trends to ensure continuity of care.

| Longitudinal History (Demo Data) | Clinical Assessment Entry |
| :---: | :---: |
| <img src="./visit-history-ui-2.png" width="350"> | <img src="./Screenshot_20251226_213334.png" width="350"> |
| **Real-time Vitals:** Pulls historical trends (Weight, BP, Sugar). | **Data Entry:** Optimized for field staff with limited digital literacy. |

### 2. Administrative & Supply Chain Logic
[cite_start]The administrative side handles the economics of humanitarian aid, providing visibility into medicine stock and automating logistics for mobile ambulance crews[cite: 12, 13].

| Inventory Management | Admin Navigation |
| :---: | :---: |
| <img src="./medicine-inventory-ui.png" width="350"> | <img src="./admin-navigation-page.png" width="350"> |
| **Smart Inventory:** Real-time tracking of life-saving stock levels. | **Admin Portal:** Centralized control for districts and clinics. |

---

## 🚀 Key Technical Innovations

* **Automated Workflow Logic:** Developed Java-based automation that handles staff clock-ins and location assignments based on the first and last patient interactions of the day.
* **Smart Inventory Intelligence:** Stock levels for life-saving medicines (e.g., Cipro-500, Amoxipen) are deducted in real-time as treatments are recorded, triggering "Low Stock" alerts for administrators.
* **Resilient Architecture:** Implemented an offline-first data persistence model. Data is stored locally and automatically synchronized with **Firebase Cloud Firestore** the moment the mobile clinic returns to a 3G/4G coverage area.
* **Administrative Analytics:** Custom data transformation layer that exports complex NoSQL database structures into organized Google Sheets for high-level organizational analysis.

---

## 🛠️ Technical Stack
* **Frontend:** Android Studio (Java)
* **Backend & Database:** Firebase Cloud Firestore
* **Impact Areas:** Rural India (Parivaar) and South Sudan (SuDRO)

<details>
<summary><b>📖 Read the Project Backstory (The "Why")</b></summary>

When I first connected with Parivaar, I found that each "tally mark" on paper was a person reduced by the limits of physical records. As a freshman at Stanford, I taught myself Android Studio to build a digital solution that preserves patient dignity and ensures life-saving longitudinal care.
</details>
