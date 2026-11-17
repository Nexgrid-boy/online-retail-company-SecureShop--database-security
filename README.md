# SecureShop: Database Security, Encryption & Vulnerability Assessment

## 📌 Project Overview
**SecureShop** is a comprehensive database security hardening and auditing project simulating an e-commerce backend environment. This project demonstrates practical implementation of database security controls, including data-at-rest encryption, dynamic masking, Role-Based Access Control (RBAC), and SQL injection vulnerability assessment.

---

## 🛠️ Tech Stack & Tools
* **Database Management System:** MySQL
* **Administration Interface:** phpMyAdmin
* **Core Concepts:** AES Encryption, Data Masking, Principle of Least Privilege, SQL Injection

---

## 🚀 Key Modules & Implementation

### 1. Database Architecture Setup
Created a relational database structure containing interconnected tables: `customers`, `orders`, `payment_details`, and `products`.

### 2. Data Protection & Masking
* **Encryption (`Task 2.1`):** Secured sensitive payment records using MySQL's built-in AES encryption functions (`AES_ENCRYPT` / `AES_DECRYPT`).
* **Data Masking (`Task 2.2`):** Applied string manipulation functions (`CONCAT`, `SUBSTRING`) to mask customer phone numbers, exposing only the last digits for operational compliance.

### 3. Access Control & Least Privilege (RBAC)
* Created a dedicated profile for a delivery role (`'Delivery Executive'@'localhost'`).
* Configured granular permissions (`GRANT SELECT, DELETE, UPDATE`) and audited access using `SHOW GRANTS`.
* Enforced security best practices by revoking unauthorized administrative privileges (`REVOKE DELETE`).

### 4. Vulnerability Assessment & SQL Injection
* Identified poorly parameterized queries joining `orders` and `customers` tables via `order_id`.
* Simulated a classic SQL injection attack (`OR 1=1`) to demonstrate logic flaw exploits and underscore the necessity of prepared statements.

---

## 📂 Repository Structure
* `sql/` - Contains all SQL scripts used across Tasks 2, 3, and 4.
* `screenshots/` - Contains lab verification screenshots.
