> # 🔒 SOURCE CODE PRIVATE
> 
> <p align="center">
>   <strong>The source code in this repository is not publicly shared.</strong><br>
>   <em>Only screenshots and documentation are displayed for portfolio/reference purposes.</em>
> </p>

---

<!-- COLOR BAR -->
<p align="center">
  <img src="https://via.placeholder.com/800x5/2c3e50/2c3e50" alt="divider" width="800" height="4">
</p>

<h1 align="center">🎓 Student-Parent Follow-up System</h1>

<p align="center">
  <strong>A Comprehensive School Management Platform Bridging Teachers, Parents, and Administration</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0-blue?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/database-MySQL-orange?style=for-the-badge&logo=mysql" alt="MySQL">
  <img src="https://img.shields.io/badge/backend-PHP-777BB4?style=for-the-badge&logo=php" alt="PHP">
  <img src="https://img.shields.io/badge/status-Completed-success?style=for-the-badge" alt="Status">
</p>

---

## 📋 Table of Contents

- [System Overview](#-system-overview)
- [User Roles](#-user-roles--access-levels)
- [Core Features](#-core-features)
- [Database Structure](#-database-structure)
- [Technology Stack](#-technology-stack)
- [Installation](#-installation)
  

---

## 📌 System Overview

The **Student-Parent Follow-up System** is a full-featured school management solution designed to streamline academic operations, enhance parent-teacher communication, and provide real-time access to student performance data.

| Aspect | Description |
|--------|-------------|
| **Purpose** | Bridge communication gap between school and parents |
| **Target Users** | Schools, Colleges, Educational Institutions |
| **Key Benefit** | Real-time tracking of student progress |
| **Deployment** | Web-based, Multi-user |

---

## 👥 User Roles & Access Levels

| Role | Badge | Permissions |
|------|-------|-------------|
| **Admin** | 🟢 | Complete system control, user management |
| **Registrar** | 🔵 | Student enrollment, class assignment |
| **Finance** | 💰 | Fee processing, payment verification |
| **Teacher** | 📚 | Grade entry, attendance marking |
| **Parent** | 👪 | View child's progress, communicate |
| **Record Office** | 📄 | Academic records & reporting |

---

## ⚡ Core Features

### 📊 Academic Management
- ✅ Daily **Attendance Tracking** with remarks
- 📝 **Grade Management** with component scores (tests, mid, assignments, final)
- 📈 **Term-based Reporting** with JSON summary storage
- 🏫 **Class & Section** organization

### 💰 Financial Management
- 💵 **Fee Structure** by class and academic year
- 🧾 **Payment Processing** with receipt upload
- 🔍 **Verification System** (Pending → Approved/Rejected)
- 📁 **Student Payment History**

### 💬 Communication
- ✉️ **Parent-Teacher Messaging**
- 📱 **Parent Portal** for real-time access
- 🔔 **Read Receipts** tracking

### 👨‍🏫 Teacher Features
- 📖 **Subject Assignment** management
- 🎯 **Grade Submission** with validation
- 👥 **Class-specific** attendance

---

## 🗄️ Database Structure

<details>
<summary><b>Click to view database schema</b></summary>

### Main Tables

| Table | Description |
|-------|-------------|
| `students` | Student profiles, class, section, division |
| `users` | System users with role-based access |
| `attendance` | Daily attendance records |
| `grades` | Student grades with component scores |
| `payments` | Fee payment transactions |
| `fees` | Fee structure by class |
| `subjects` | Subject master list |
| `teachers` | Teacher profiles |
| `messages` | Parent-teacher communication |
| `grade_reports` | JSON-based term reports |

### Supporting Tables

| Table | Purpose |
|-------|---------|
| `students_temp` | Temporary enrollment applications |
| `parent_student` | Parent-child relationship mapping |
| `teacher_assignments` | Subject & class allocation |

### Key Relationships
students (1) ──────< (M) attendance
students (1) ──────< (M) grades
students (M) ──────> (M) users (via parent_student)
teachers (M) ──────> (1) users
payments (M) ──────> (1) students_temp

</details>

---

## 🛠️ Technology Stack

<p align="center">
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white" alt="PHP">
  <img src="https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white" alt="MariaDB">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript">
</p>

| Layer | Technology |
|-------|------------|
| **Database** | MySQL / MariaDB 10.4+ |
| **Backend** | PHP 8.2+ |
| **Frontend** | HTML5, CSS3, JavaScript |
| **Authentication** | Session-based with bcrypt hashing |
| **Data Format** | JSON for reports |

---

## 🚀 Installation

<details>
<summary><b>Quick Setup Guide</b></summary>

### Prerequisites
- XAMPP / WAMP / LAMP stack
- PHP 8.2+
- MySQL 10.4+

### Steps

```bash
# 1. Clone or import database
- Run the SQL dump file in phpMyAdmin

# 2. Configure database connection
- Update config.php with your credentials

# 3. Default Admin Login
Username: admin1
Password: password

# 4. Access the system
http://localhost/student_system
```
### Default User Accounts

| Username | Role | Password |
|----------|------|----------|
| admin1 | Admin | password |
| registrar1 | Registrar | password |
| finance1 | Finance | password |
| math.teacher | Teacher | password |
| parent1 | Parent | password |
| record1 | Record Office | password |

</details>

---

## 📄 License

<div align="center">

This project is for demonstration purposes only.

© 2025 Student-Parent Follow-up System

</div>
