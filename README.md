> # 🔒 SOURCE CODE PRIVATE
>
> <p align="center">
>   <strong>The source code in this repository is not publicly shared.</strong><br>
>   <em>Only screenshots and documentation are displayed for portfolio/reference purposes.</em>
> </p>

---

<p align="center">
  <img src="https://via.placeholder.com/800x5/2c3e50/2c3e50" alt="divider" width="800" height="4">
</p>

<h1 align="center">🎓 Student-Parent Follow-up System</h1>

<p align="center">
  <strong>School Management Platform Bridging Teachers, Parents, and Administration</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0-blue?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/Database-MySQL-orange?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/Backend-PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP">
  <img src="https://img.shields.io/badge/status-Completed-success?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/Team-Collaborative%20Build-ff6b35?style=for-the-badge" alt="Team">
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

| Aspect | Details |
|--------|---------|
| **Purpose** | Bridge the communication gap between school and parents |
| **Target Users** | Schools, Colleges, and Educational Institutions |
| **Key Benefit** | Real-time tracking of student progress |
| **Deployment** | Web-based, Multi-user |
| **Project Type** | Collaborative Academic / Capstone Project |

---

## 👨‍💻 Team

> This system was collaboratively built by a team as part of an academic capstone project.

| Role | Responsibility |
|------|---------------|
| **Full Stack Developer** | Backend logic, database design |
| **Frontend Developer** | UI/UX, HTML/CSS/JS |
| **Database Administrator** | Schema design, relationships |
| **QA / Testing** | Validation, bug reporting |

> *Update this table with your actual team members and their roles.*

---

## 👥 User Roles & Access Levels

| Role | Icon | Permissions |
|------|------|-------------|
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
- 📝 **Grade Management** with component scores — tests, midterms, assignments, and finals
- 📈 **Term-based Reporting** with JSON summary storage
- 🏫 **Class & Section** organization

### 💰 Financial Management
- 💵 **Fee Structure** by class and academic year
- 🧾 **Payment Processing** with receipt upload
- 🔍 **Verification Workflow** — Pending → Approved / Rejected
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
<summary><b>📂 Click to expand database schema</b></summary>

<br>

### 🗃️ Main Tables

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

### 🔗 Supporting Tables

| Table | Purpose |
|-------|---------|
| `students_temp` | Temporary enrollment applications |
| `parent_student` | Parent-child relationship mapping |
| `teacher_assignments` | Subject & class allocation |

### 📐 Key Relationships
students (1) ──────< (M) attendance
<br>
students (1) ──────< (M) grades
<br>
students (M) ──────> (M) users (via parent_student)
<br>
teachers (M) ──────> (1) users
<br>
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
| **Data Format** | JSON for term reports |

---

## 🚀 Installation

<details>
<summary><b>⚙️ Click to expand setup guide</b></summary>

<br>

### ✅ Prerequisites

- XAMPP / WAMP / LAMP stack
- PHP 8.2+
- MySQL / MariaDB 10.4+

### 🧭 Steps

```bash
# 1. Import the database
#    Open phpMyAdmin and run the provided SQL dump file

# 2. Configure the database connection
#    Edit config.php with your local credentials

# 3. Launch the application
#    http://localhost/student_system
```

### 🔑 Default User Accounts

| Username | Role | Password |
|----------|------|----------|
| `admin1` | Admin | `password` |
| `registrar1` | Registrar | `password` |
| `finance1` | Finance | `password` |
| `math.teacher` | Teacher | `password` |
| `parent1` | Parent | `password` |
| `record1` | Record Office | `password` |

> ⚠️ **Note:** Change all default passwords immediately after first login.

</details>

---

📞 Contact
<div align="center">

**For inquiries about this project, please reach out directly.**

<br>

<a href="mailto:boxctf76@gmail.com">
  <img src="https://img.shields.io/badge/Email-boxctf76%40gmail.com-red?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
</a>

<a href="https://linkedin.com/in/abduselam-kedir-5945732a6" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
</a>

</div>
