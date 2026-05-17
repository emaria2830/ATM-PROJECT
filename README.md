# 🏦 ATM System in C (Bank Simulation Project)

This project is a console-based ATM (Automated Teller Machine) simulation written in C.  
It simulates a basic banking system with account management, secure PIN authentication, transaction handling, and persistent file storage.

---

## 📌 Project Overview

The system allows users to:

- Create new bank accounts
- Log in using a 4-digit PIN
- Perform banking operations (deposit, withdraw, transfer)
- View account balance
- Change PIN securely
- Delete account
- Track transaction history during session
- Store all data persistently using file I/O

This project was developed as a learning exercise in **C programming, file handling, and system-level logic design**.

---

## ⚙️ Features

### 🔐 Authentication
- PIN-based login system
- 3 incorrect attempts → account access blocked (session-level)

### 💳 Account System
- Auto-generated 12-digit unique account numbers
- Multiple account support (up to 100 users)
- Account creation via guest mode

### 💰 Banking Operations
- Deposit money
- Withdraw money with:
  - Daily withdrawal limit (5000 TL)
  - Balance validation
- Money transfer between accounts

### 🧾 Account Management
- PIN change (with verification)
- Account deletion
- Real-time account updates

### 📊 System Features
- Transaction history (session-based)
- File-based persistence (`hesaplar.txt`)
- Automatic data loading on startup
- Date & time tracking using `time.h`

---

## 🧠 Technical Highlights

- Struct-based data modeling (`struct hesap`, `BankaDurumu`)
- Pointer usage for system state management
- Modular function design
- File I/O (`fopen`, `fprintf`, `fscanf`)
- Random unique ID generation
- Input validation & error handling
- Localized time formatting (`setlocale`, `strftime`)
- Menu-driven state machine logic

---

## 🗂️ Data Storage Format

Accounts are stored in:

Accounts are stored in the file hesaplar.txt. Each account is saved in a single line containing five values: account number, PIN, balance, daily withdrawal amount, and last withdrawal date. This structure allows the program to load all user data automatically when the system starts and update it whenever a transaction occurs. The file is rewritten after each important operation such as deposit, withdrawal, transfer, account creation, PIN change, or account deletion, ensuring data consistency between sessions.
