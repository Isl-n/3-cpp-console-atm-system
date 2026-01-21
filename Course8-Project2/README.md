# C++ Console ATM System

A console-based **ATM simulation** written in C++ that allows clients to log in using an account number and PIN, then perform common banking operations through a menu-driven interface.

The project focuses on **procedural programming**, file handling, and input validation.

---

## ✨ Features

- Client login using:
  - Account Number
  - PIN Code
- ATM operations:
  - Quick Withdraw (predefined amounts)
  - Normal Withdraw (custom amount, multiple of 5)
  - Deposit
  - Check account balance
- Balance validation (prevents overdraft)
- File-based persistence using a text file
- Clear, menu-driven console UI

---

## 🏧 ATM Menu Options

After successful login, the client can:
1. Quick Withdraw (20, 50, 100, 200, …)
2. Normal Withdraw
3. Deposit
4. Check Balance
5. Logout

Quick Withdraw provides predefined amounts for faster transactions.

---

## 🗂️ Data Storage

- File: `Clients.txt`
- Format per line:
```text
AccountNumber#//#PinCode#//#Name#//#Phone#//#Balance
```
The file is read on login and updated after each transaction.

```text
On login, the system validates the account number and PIN against records stored in `Clients.txt` and loads the client’s data into memory.
```
---

## 📄 Sample Clients File

A sample `Clients.txt` file is included in the repository for testing and demonstration purposes.

```text
A1001#//#1111#//#Ahmad Ali#//#0591234567#//#1500.50
A1002#//#2222#//#Sara Noor#//#0597654321#//#320.00
A1003#//#3333#//#Omar Hassan#//#0521112233#//#9999.99
A1004#//#4444#//#Lina Khaled#//#0549876543#//#75.25
A1005#//#5555#//#Yousef Saleh#//#0505556677#//#12000.00
```

**Example Login:**  
Account Number: `A1001`  
PIN: `1111`

---

## 📝 Notes

- This project is written in a **procedural style** using functions and structs.
- No database is used — data persistence is handled via text files.
- Uses `system("cls")` and `system("pause>0")` (Windows console behavior).
- Intended for learning and practice purposes (ATM logic & flow simulation).

---

## 🚀 Build & Run

Compile with any C++ compiler:

```bash
g++ main.cpp -o ATM
./ATM