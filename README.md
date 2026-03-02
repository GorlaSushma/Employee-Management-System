# Employee-Management-System
Developing a web application that allows administrators to perform CRUD (Create, Read, Update, Delete) operations on employee records.   Ensureing the system has proper validation and authentication mechanisms to protect sensitive employee data.

Here is a clean and professional `README.md` file for your project:

---

# Employee Management System

A simple **Employee Management System (EMS)** built using **HTML, CSS, and Vanilla JavaScript**.
This application allows admin users to register, log in securely (with hashed passwords), and manage employee records using browser `localStorage`.

---

## 📌 Features

### 🔐 Authentication

* Admin Signup
* Admin Login
* Password hashing using **SHA-256**
* Session management using `localStorage`
* Logout functionality

### 👨‍💼 Employee Management (CRUD)

* Add new employees
* View employee list
* Delete employees
* Unique employee IDs using `crypto.randomUUID()`

### 🎨 UI Features

* Clean, modern card-based design
* Floating label form inputs
* Responsive centered layout
* Simple employee table view

---

## 🛠️ Technologies Used

* **HTML5** – Structure
* **CSS3** – Styling & layout
* **JavaScript (ES6+)** – Logic & interactivity
* **Web Crypto API (SHA-256)** – Password hashing
* **Web Storage API (localStorage)** – Data persistence

---

## 📂 Project Structure

```
EmployeeManagementSystem/
│
└── index.html   # Complete application (UI + Logic)
```

---

## 🚀 How It Works

### 1️⃣ Admin Registration

* User enters username, email, and password.
* Password is hashed using **SHA-256**.
* Data is stored in `localStorage` under:

  ```
  user_<username>
  ```
* Duplicate usernames are prevented.

---

### 2️⃣ Admin Login

* User enters credentials.
* Input password is hashed.
* System compares hashed values.
* On success:

  * `sessionUser` is stored in `localStorage`
  * Dashboard is displayed.

---

### 3️⃣ Employee Dashboard

Once logged in, the admin can:

#### ➕ Add Employee

* Enter name, email, and position.
* Employee is stored in `localStorage` under:

  ```
  employees
  ```

#### 📋 View Employees

* Employees are dynamically loaded into a table.

#### ❌ Delete Employee

* Removes employee using unique `id`.

---

## 🔑 Data Storage Format

### User Object

```json
{
  "email": "admin@email.com",
  "password": "hashed_password_here"
}
```

### Employee Object

```json
{
  "id": "uuid",
  "name": "John Doe",
  "email": "john@email.com",
  "position": "Developer"
}
```

---

## ⚠️ Security Notice

Although passwords are hashed using SHA-256:

* This project still uses **localStorage**
* No backend validation
* No database
* No HTTPS enforcement
* No salting mechanism

⚠️ **This project is for learning/demo purposes only.**

For production applications:

* Use a secure backend (Node.js, Django, etc.)
* Store passwords with salted hashing (bcrypt)
* Use authentication tokens (JWT)
* Implement server-side validation
* Use HTTPS

---

## 🔮 Possible Improvements

* Add edit/update employee functionality
* Add form validation messages
* Implement search and filter
* Add role-based access control
* Store data in a real database
* Add pagination
* Improve UI with animations
* Add dark mode

---

## 📸 Application Flow

1. Signup →
2. Login →
3. Dashboard →
4. Add/View/Delete Employees →
5. Logout

---

## 📄 License

This project is open-source and free to use for educational purposes.

---

