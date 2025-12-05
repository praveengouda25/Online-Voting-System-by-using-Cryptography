# Online-Voting-System-by-using-Cryptography
A secure and user-friendly online voting platform that enables citizens to cast votes digitally.   The system uses cryptographic techniques such as password hashing to protect user credentials, prevent vote tampering, and ensure election integrity.

# ONLINE VOTING SYSTEM USING CRYPTOGRAPHY

A secure and user-friendly online voting platform that enables citizens to cast votes digitally.  
The system uses cryptographic techniques such as password hashing to protect user credentials, prevent vote tampering, and ensure election integrity.

---

## 📌 Table of Contents
- [Project Overview](#project-overview)  
- [Features](#features)  
- [System Workflow](#system-workflow)  
- [Pages & Screens](#pages--screens)  
- [Technology Stack](#technology-stack)  
- [Installation & Setup](#installation--setup)  
- [How to Run](#how-to-run)  
- [Screenshots](#screenshots)  
- [Future Enhancements](#future-enhancements)  
- [Authors](#authors)

---

## 📘 Project Overview

This project provides a digital platform where registered users can securely cast their vote online.  
The system uses **SHA-256 hashing** to store passwords securely and follows strict validation rules to prevent unauthorized access and double voting.

It reduces manual workload, ensures faster result generation, and enables voting from any location—beneficial for elderly, physically challenged, and remote citizens.

---

## ⭐ Features

- Secure admin login  
- Voter registration with unique ID generation  
- Password hashing for secure authentication  
- Voter login with validation  
- Cast-vote page with selectable candidates  
- Prevention of duplicate voting  
- Live vote count display for admin  
- Multi-window support  
- Centralized vote storage using CSV and DataFrames  
- Thread-based concurrent connections for multiple voters  

---

## 🔄 System Workflow

1. **Admin Logs In**
   - Starts the election server  
   - Registers voters  
   - Monitors vote count  

2. **Voter Registration**
   - Admin registers voters with details such as name, zone, city, and password  
   - System generates a unique voter ID  

3. **Voter Login**
   - Voter enters ID and password  
   - System verifies hashed credentials  
   - System checks if the voter has already cast a vote  

4. **Casting the Vote**
   - Voter selects a candidate from the list  
   - System encrypts and stores the vote  
   - Vote status updates to “cast”  

5. **Counting & Results**
   - Admin views total votes for each candidate  
   - Results are displayed instantly  

---

## 🖥 Pages & Screens

### **Home Page**
- Entry point for all users  
- Buttons for:  
  - **Admin Login**  
  - **Voter Login**  
  - **New Window**

### **Admin Login Page**
Fields:
- Admin ID  
- Password  

Admin can:
- Start the server  
- Register new voters  
- View vote counts  

### **Voter Registration Page**
Fields:
- Name  
- Gender  
- Zone  
- City  
- Password  

The system:
- Generates voter ID  
- Stores data securely  
- Prepares credentials for login

### **Voter Login Page**
Voter enters:
- Voter ID  
- Password  

System validation ensures:
- Correct credentials  
- Voter has not voted already  

### **Cast Vote Page**
Contains:
- Candidate list (e.g., BJP, Congress, others)  
- Submit button  

System ensures:
- One vote per user  
- Secure vote storage  

### **Admin Dashboard / Results**
Admin can:
- View total votes for each party  
- Monitor election progress  

---

## 🔐 Cryptography & Security

- **SHA-256 password hashing**  
- Passwords are not stored or visible anywhere in plain text  
- Authentication is validated by hashing input and comparing hashes  
- Votes stored securely in CSV and DataFrame structures  
- Duplicate voting prevented through voter status flags  
- Server uses thread-based handling for safe multi-voter access  

---

## 🛠 Technology Stack

**Programming Language:** Python  
**Libraries & Modules:**  
- Pandas  
- Tkinter  
- Socket  
- Threading  
- Subprocess  
- Hashlib  

**Database:** CSV files (used with pandas DataFrames)  
**Interface:** Tkinter-based GUI  
**Server Model:** Multi-threaded TCP socket server  

---

## ⚙️ Installation & Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/online-voting-system.git

2. Install Python 3.x

3. Install required libraries:
   pip install pandas

4.No database setup needed — system uses CSV auto-generation

5. Ensure Python is added to PATH


##  Future Enhancements

Blockchain-based vote validation

Two-factor authentication (OTP, biometrics)

Mobile application support

Stronger encryption for vote data

Multilingual interface

Cloud-based scalable server

Accessibility-enhanced UI
