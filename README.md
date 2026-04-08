# Clinic-Management-ERD
Worked on building an ER diagram for a clinic system covering appointments, consultations, diagnostics, reports, and payments.

# 🏥 Clinic Appointment & Diagnostics ERD

This project contains the Entity Relationship Diagram (ERD) for a clinic management system designed to handle appointments, consultations, diagnostic tests, reports, and payments in a structured and scalable way.

---

## 📌 Features

* 👤 Patient Management
* 👨‍⚕️ Doctor & Specialization Management
* 📅 Appointment Booking System
* 🩺 Consultation (Visit) Tracking
* 🧪 Diagnostic Test Prescription
* 📄 Report Generation
* 💳 Payment Management

---

## 🧠 Key Design Decisions

* **Appointment vs Consultation**

  * Appointment = booking
  * Consultation = actual visit
  * Not all appointments result in consultations

* **Test Management**

  * Tests are linked to consultations (not appointments)
  * One consultation can have multiple tests

* **Many-to-Many Handling**

  * Consultation ↔ Tests handled via `consultation_tests` junction table

* **Report Linking**

  * Reports are generated per test instance (not directly per patient)

* **Flexible Payments**

  * Payments can be linked to either appointments or consultations

---

## 🧩 Entities Included

* Patients
* Doctors
* Specializations
* Appointments
* Consultations
* Tests
* Consultation Tests
* Reports
* Payments

---

## 🔗 Relationships Overview

* One Patient → Many Appointments
* One Doctor → Many Appointments
* One Appointment → Zero or One Consultation
* One Consultation → Many Tests
* One Test → Used in Many Consultations
* One Test Instance → One Report
* One Patient → Many Payments

---

## 🛠️ Tools Used

* Eraser (for ER Diagram using code-based modeling)

---

## 📷 ER Diagram

> Add your exported image or diagram link here
> Example:
> ![ER Diagram](./diagram.png)

---

## 🚀 How to Use

1. Open Eraser / supported ER tool
2. Paste the ERD code
3. Generate the diagram
4. Export as PNG or PDF

---

## 📈 Future Improvements

* Add prescription tracking
* Add user authentication system
* Integrate insurance handling
* Build backend APIs (Node.js + Express)

---

## 👨‍💻 Author

* Mahesh Dhondge

---

## ⭐ Acknowledgement

This project was created as part of a Web Development Cohort assignment focusing on database design and ER modeling.

---
