# User Management Task  

This project implements a modular user management system using **PostgreSQL** as the database. The task includes creating database migrations, a reusable user package, and three APIs for user sign-up, sign-in, and listing users.  

---

## Requirements  

### Database  
- **PostgreSQL**  

### Migrations  
1. **Migration 1:**  
   - Create a `user` table with the following fields:  
     - `email` (string)  
     - `password` (string, encrypted)  

2. **Migration 2:**  
   - Add the following fields to the `user` table:  
     - `FirstName` (string)  
     - `LastName` (string)  

---

## APIs  

### 1. User Sign-Up API  
- **Purpose:** Allows users to create an account.  
- **Input:** `email`, `password`, `FirstName`, `LastName`  
- **Processing:** Encrypts the password before saving it in the database.  
- **Response:** Success or error message.  

### 2. User Sign-In API  
- **Purpose:** Authenticates users based on their credentials.  
- **Input:** `email`, `password`  
- **Processing:** Validates the credentials.  
- **Response:** Success response or authentication error.  

### 3. User Listing API  
- **Purpose:** Lists all registered users.  
- **Processing:** Fetches users from the database, excluding sensitive fields like passwords.  
- **Response:** A list of users.  

---

## Development Structure  

- **User Package:**  
  A modular and reusable package containing the core functionality for managing users, including:  
  - Database interactions.  
  - Encryption for passwords.  
  - User validation logic.  

---
