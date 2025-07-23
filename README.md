# 🏦 Banking Management System using Python & MySQL

Welcome to the **Banking Management System** project, developed as part of a hands-on learning experience in Python and MySQL integration. This system simulates a virtual bank named **Colony Bank of India**, designed to help bank staff manage customer records efficiently.

## 📌 Project Overview

This project allows authorized users to:
- Create new customer records
- View all customer records
- Update existing records
- Delete customer records
- Manage customer transactions
- Update loan details

All data is stored in a **MySQL database**, and the interface is built using **Python**, with a strong focus on **exception handling** for user-friendly interactions.

## 🛠️ Technologies Used

- **Frontend**: Python (with `datetime`, `mysql.connector`)
- **Backend**: MySQL
- **IDE**: Visual Studio Code / IDLE

## 📂 Files Included

```
Banking_Management_Python_DB/
│
├── bank-project.py     # Main Python script
├── README.md           # Project documentation
```

## 🧰 Requirements

- Python (latest version)
- MySQL Server
- MySQL Connector for Python
- Visual Studio Code or IDLE

## 🗃️ MySQL Database Setup

### 🔹 Bank Table
```sql
CREATE TABLE bank (
  name VARCHAR(30),
  UserName VARCHAR(30),
  password TINYTEXT,
  Date_of_birth DATE,
  address VARCHAR(40),
  Mobile_Number VARCHAR(30),
  Aadhar_no VARCHAR(30),
  Balance INT,
  PRIMARY KEY (UserName)
);
```

### 🔹 Transaction Table
```sql
CREATE TABLE Transaction (
  credited INT,
  debited INT,
  username1 VARCHAR(20),
  FOREIGN KEY (username1) REFERENCES bank(UserName)
);
```

## 🔐 Authentication

- Only authorized users can access the system.
- New users can register with a username and password.
- Login credentials are verified before granting access.

## 💡 Features

- Full CRUD operations on customer data
- Transaction tracking (credit/debit)
- Loan management
- Secure login system
- Exception handling for robust performance

## 📌 Suggestions

- Run `bank-project.py` in **IDLE** for best compatibility.
- Ensure the MySQL tables (`bank` and `Transaction`) are created before running the script.

## 📞 Contact

For queries or contributions, visit the GitHub Profile.
