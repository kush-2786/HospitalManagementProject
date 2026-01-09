# HospitalManagementProject
______________________________

Hospify is a simple **Hospital Management System** made using **JavaFX** and **MySQL**.
It helps to manage:

- Patients
- Doctors
- Appointments

---

## Features

### Patients
- Add patient (Name, Age, Gender, City)
- View all patients in table

### Doctors
- Add doctor (Name, Speciality)
- View all doctors in table

### Appointments
- Schedule appointment using Patient ID, Doctor ID and Date
- View all appointments in table

---

## Tech Used
- Java
- JavaFX
- MySQL
- JDBC

---

## Database Setup

Create database:

```sql
CREATE DATABASE Hospital;
USE Hospital;
CREATE TABLE patients (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    gender VARCHAR(10),
    city VARCHAR(50)
);

CREATE TABLE doctors (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    speciality VARCHAR(50)
);

CREATE TABLE appointments (
    patient_id INT,
    doctor_id INT,
    appointment_date VARCHAR(20),
    FOREIGN KEY (patient_id) REFERENCES patients(id),
    FOREIGN KEY (doctor_id) REFERENCES doctors(id)
);
```

#How to Run

1. Open the project in IntelliJ / Eclipse

2. Setup JavaFX in your IDE

3. Update MySQL password in JavaApp.java

4. Run JavaApp.java
