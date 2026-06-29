# 🏨 Hotel Management System

> A relational database project designed to digitize and streamline hotel operations — covering guest management, room bookings, payments, employee records, and hotel services.

> 📌 *CSE 212 — Database Systems Lab, University of Asia Pacific (UAP), Semester 2.2*

---

## 📄 Repository Contents

```
Hotel-Management-System/
├── docs/
│   └── Hotel_Management_System.pdf          # Full project report (26 pages)
├── diagrams/
│   ├── Hotel_Management_System_ER_.png      # Entity-Relationship Diagram
│   └── Schema_Hotel_Management_System_.png  # Schema Diagram
├── sql/
│   ├── Hotel_Management_System_Table.sql    # Table creation scripts
│   └── Hotel_Management_System_Data.sql     # Data insertion scripts
└── README.md
```

---

## 🎯 Objective

Design and implement a Hotel Management System that efficiently manages:
- Guest registrations and personal information
- Room bookings, check-in & check-out tracking
- Payment processing with discount support
- Room availability and room type management
- Employee records and role assignments
- Hotel services availed by guests

---

## 🗂️ Database Schema

The system contains **10 tables** with proper relationships:

| Table | Description |
|-------|-------------|
| `Hotel` | Hotel details — name, location, contact |
| `Room` | Room info — number, type, availability status |
| `RoomType` | Room categories with price per night |
| `Guest` | Guest personal information |
| `Booking` | Room reservations with check-in/out dates |
| `Payment` | Payment records with method and discount |
| `Service` | Services availed by guests during their stay |
| `Employee` | Staff information per hotel |
| `Role` | Job roles for employees |
| `Emp_Role` | Employee-role linking table with shift info |

---

## 🔗 Key Relationships

- **Hotel → Room** (One-to-Many)
- **Hotel → Employee** (One-to-Many)
- **Guest → Booking** (One-to-Many)
- **Guest → Payment** (One-to-Many)
- **Booking → Room** (One-to-One)
- **Room → RoomType** (Many-to-One)
- **Employee → Role** via `Emp_Role` (Many-to-Many)

---

## ⚙️ Database Objects

| Object | Name | Purpose |
|--------|------|---------|
| Trigger | `After_Booking_Guest` | Auto-updates room status to 'Occupied' after a new booking |
| View | `room_view` | Displays room ID, number, and status |
| Function | `Total_Payment` | Returns total payment amount for a given guest |
| Stored Procedure | `Daily_Payment_Calc` | Returns total payments for a specific date |

---

## 🛠️ Tech Stack

![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![SSMS](https://img.shields.io/badge/SSMS-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)

- **Database:** Microsoft SQL Server
- **Tool:** SQL Server Management Studio (SSMS)
- **Concepts:** ER Modeling, Schema Design, Normalization, DDL, DML, Joins, Subqueries, Triggers, Views, Functions, Stored Procedures

---

## 🚀 How to Run

1. Open **SQL Server Management Studio (SSMS)**
2. Run `Hotel_Management_System_Table.sql` to create the database and tables
3. Run `Hotel_Management_System_Data.sql` to insert sample data
4. Execute any query from the project report to explore the data

---

## 👥 Team

| Name | ID |
|------|----|
| Md. Momin Ali Rifat | 23201009 |
| Nazmuz Saif | 23201023 |
| Kamrul Hasan Siam | 23201033 |
| Tahsin Rahman Khan | 23201050 |

**Submitted To:** Nadeem Ahmed, Assistant Professor, CSE, UAP
**Course:** Database Systems Lab (CSE 212)

---

## 📬 Contact

**Nazmuz Saif**
🌐 [nazmuzsaif.onrender.com](https://nazmuzsaif.onrender.com)
💼 [LinkedIn](https://www.linkedin.com/in/nazmuzsaif/)
🐙 [GitHub](https://github.com/Nazmuz-Saif)
