# ☁️ Cloud-Based Assignment Portal

A modern **Cloud-Based Assignment Portal** built using **React.js and Firebase** that provides a centralized platform for managing academic assignments, submissions, and student information.

The application demonstrates practical implementation of **Cloud Computing, Firebase Authentication, Cloud Firestore, CRUD operations, role-based access, and responsive web development**.

---

## 📌 Project Overview

Managing assignments through messages, emails, or physical submissions can become difficult for both students and teachers.

The **Cloud-Based Assignment Portal** provides a centralized digital platform where:

* 👨‍🏫 Teachers can create and manage assignments.
* 👨‍🎓 Students can view available assignments.
* 📄 Students can submit their work.
* 📊 Assignment information can be managed through the cloud.
* 🔐 Users can access the system through authentication.
* ☁️ Academic data can be stored using Cloud Firestore.

The project is designed as an educational cloud-computing application.

> **Note:** This implementation can use Firebase Authentication and Cloud Firestore without requiring Firebase Storage. If actual assignment-file uploads are added later, a file-storage service can be integrated separately.

---

# ✨ Features

## 🔐 Authentication

Users can:

* Register an account
* Login
* Logout
* Access their personalized dashboard
* Use role-based application functionality

Authentication is handled using **Firebase Authentication**.

---

# 👨‍🏫 Teacher / Faculty Features

Teachers can:

* Create assignments
* Add assignment title
* Add description
* Set deadline
* Add subject/category
* View created assignments
* Monitor student submissions
* Manage assignment information

Example:

```text id="x0x1pr"
Assignment Title: Database Management System
Subject: DBMS
Deadline: 15 October 2026
Description: Complete the given SQL queries.
```

---

# 👨‍🎓 Student Features

Students can:

* View available assignments
* Read assignment details
* Check deadlines
* Submit assignments
* View submission status
* Track assigned work
* Access their personalized dashboard

---

# 📚 Assignment Management

Each assignment can contain:

* Assignment title
* Subject
* Description
* Deadline
* Teacher ID
* Created date
* Status

Example:

```text id="6q9t0j"
Assignment
│
├── Title
├── Subject
├── Description
├── Deadline
├── Teacher ID
├── Created At
└── Status
```

---

# 📝 Submission Management

Students can submit assignment information through the portal.

A submission can contain:

```text id="3czpzw"
Submission
│
├── Assignment ID
├── Student ID
├── Student Name
├── Submission Date
├── Status
└── Remarks
```

Possible submission statuses:

```text id="nqvl1c"
Not Submitted
Submitted
Late
Reviewed
```

---

# ⏰ Deadline Tracking

The portal can display assignment deadlines so students can identify upcoming submissions.

Example:

```text id="y2l6m3"
📚 Web Development
Deadline: 10 October 2026

⏳ Status: Pending
```

---

# ☁️ Cloud-Based Data Management

The project uses **Cloud Firestore** to store application data.

Firestore can store:

* User profiles
* Assignments
* Submissions
* Subjects
* Assignment status

Data is retrieved dynamically by the React application.

---

# 📱 Responsive Interface

The portal is designed to work across:

* 💻 Desktop
* 💻 Laptop
* 📱 Mobile
* 📱 Tablet

---

# 🛠️ Technologies Used

| Technology              | Purpose                 |
| ----------------------- | ----------------------- |
| React.js                | Frontend development    |
| Vite                    | Development environment |
| JavaScript              | Application logic       |
| Firebase Authentication | User authentication     |
| Cloud Firestore         | Cloud database          |
| HTML5                   | Application structure   |
| CSS3                    | Styling                 |
| Git                     | Version control         |
| GitHub                  | Repository hosting      |

---

# ☁️ Cloud Architecture

```text id="h6qyl7"
                       ┌──────────────────┐
                       │      User        │
                       │ Web Browser      │
                       └────────┬─────────┘
                                │
                                ▼
                       ┌──────────────────┐
                       │   React + Vite   │
                       │    Frontend      │
                       └────────┬─────────┘
                                │
                  ┌─────────────┴─────────────┐
                  │                           │
                  ▼                           ▼
         ┌─────────────────┐         ┌──────────────────┐
         │ Firebase Auth   │         │ Cloud Firestore  │
         │                 │         │                  │
         │ Login/Register  │         │ Assignments      │
         │ User Sessions   │         │ Submissions      │
         └─────────────────┘         │ User Data        │
                                     └──────────────────┘
```

---

# 👥 User Roles

The application can support two main roles:

```text id="8yl1sy"
          Assignment Portal
                 │
          ┌──────┴──────┐
          │             │
          ▼             ▼
       Teacher        Student
          │             │
          ▼             ▼
 Create Assignment   View Assignment
 Manage Assignment  Submit Assignment
 View Submissions   Track Status
```

---

# 📂 Project Structure

```text id="y6iz5p"
cloud-assignment-portal/
│
├── public/
│
├── src/
│   ├── assets/
│   ├── App.jsx
│   ├── App.css
│   ├── firebase.js
│   └── main.jsx
│
├── .gitignore
├── index.html
├── package.json
├── package-lock.json
└── README.md
```

---

# ⚙️ Installation

## 1. Clone the Repository

```bash id="d3zv76"
git clone https://github.com/YOUR-USERNAME/cloud-assignment-portal.git
```

Move into the project directory:

```bash id="6kq2j8"
cd cloud-assignment-portal
```

---

## 2. Install Dependencies

```bash id="q5i8w0"
npm install
```

---

## 3. Start the Development Server

```bash id="p3q9f5"
npm run dev
```

The application will be available at a local URL similar to:

```text id="l5m9o1"
http://localhost:5173/
```

Open the URL in your browser.

---

# 🔥 Firebase Setup

## Step 1 — Create Firebase Project

Create a new project in the Firebase Console.

Enable:

```text id="9x2m7a"
Firebase Authentication
Cloud Firestore
```

Firebase Storage is **not required** for the basic version.

---

## Step 2 — Enable Authentication

Navigate to:

```text id="q2m6yw"
Firebase Console
        ↓
Authentication
        ↓
Sign-in method
        ↓
Email/Password
```

Enable:

**Email/Password**

---

## Step 3 — Create Firestore Database

Navigate to:

```text id="7g7q1h"
Firebase Console
        ↓
Firestore Database
        ↓
Create Database
```

Create the database.

---

## Step 4 — Register the Web App

Navigate to:

```text id="t8qj8u"
Project Settings
        ↓
Your Apps
        ↓
Web App
```

Register the React application.

Firebase will provide configuration values such as:

```text id="z6g5j4"
apiKey
authDomain
projectId
storageBucket
messagingSenderId
appId
```

Add the required values to:

```text id="7n9c5v"
src/firebase.js
```

---

# 🗄️ Firestore Database Structure

A simple database structure can be used.

## Users

```text id="y0q0o8"
users
 └── userId
      ├── name
      ├── email
      └── role
```

Possible roles:

```text id="2i9c47"
teacher
student
```

---

## Assignments

```text id="4j4t0h"
assignments
 └── assignmentId
      ├── title
      ├── subject
      ├── description
      ├── deadline
      ├── teacherId
      ├── status
      └── createdAt
```

---

## Submissions

```text id="v4r0dd"
submissions
 └── submissionId
      ├── assignmentId
      ├── studentId
      ├── studentName
      ├── submittedAt
      ├── status
      └── remarks
```

---

# 🔄 Application Workflow

```text id="i3u5n4"
                         START
                           │
                           ▼
                    Create Account
                           │
                           ▼
                         Login
                           │
                 ┌─────────┴─────────┐
                 │                   │
                 ▼                   ▼
              Teacher             Student
                 │                   │
                 ▼                   ▼
          Create Assignment     View Assignment
                 │                   │
                 ▼                   ▼
          Store in Firestore     Submit Work
                 │                   │
                 └─────────┬─────────┘
                           ▼
                    Cloud Firestore
                           │
                           ▼
                    Updated Records
```

---

# 📊 Example Dashboard

## Teacher Dashboard

```text id="p0pj2b"
┌─────────────────────────────────────┐
│         Teacher Dashboard           │
├─────────────────────────────────────┤
│                                     │
│  Total Assignments        12        │
│  Total Submissions        48        │
│  Pending Reviews          15        │
│                                     │
│  [+ Create Assignment]              │
│                                     │
└─────────────────────────────────────┘
```

---

## Student Dashboard

```text id="w1x7cg"
┌─────────────────────────────────────┐
│         Student Dashboard           │
├─────────────────────────────────────┤
│                                     │
│  Total Assignments        8         │
│  Submitted                5         │
│  Pending                  3         │
│                                     │
│  Upcoming Assignments               │
│                                     │
└─────────────────────────────────────┘
```

---

# 🎯 Learning Objectives

This project provides practical experience with:

* ☁️ Cloud Computing
* 🔥 Firebase
* 🔐 Firebase Authentication
* 🗄️ Cloud Firestore
* ⚛️ React.js
* 💻 JavaScript
* 🔄 CRUD Operations
* 👥 Role-Based Access
* 📚 Assignment Management
* 📝 Submission Tracking
* 📱 Responsive Web Development
* 🔧 Git & GitHub

---

# 🔐 Security

Firebase Authentication is used to authenticate users.

Firestore Security Rules should be configured so that:

* Students can access appropriate assignment information.
* Students can create their own submissions.
* Teachers can manage assignments they created.
* Unauthorized users cannot modify other users' records.

User records should be associated with the authenticated Firebase UID.

---

# 🚀 Future Enhancements

The project can be upgraded with:

* 📎 Assignment file uploads
* 📧 Email notifications
* 🔔 Deadline reminders
* 📊 Teacher analytics
* 📈 Student performance analytics
* 🗓️ Academic calendar
* 🔍 Assignment search and filtering
* 📝 Online assignment evaluation
* ⭐ Marks and grading system
* 💬 Teacher-student comments
* 🌙 Dark mode
* 📱 Progressive Web App
* 🌐 Firebase Hosting deployment

---

# 📸 Screenshots

Recommended screenshots:

<img width="1366" height="768" alt="Screenshot 2026-09-29 184745" src="https://github.com/user-attachments/assets/2c2e32a9-1933-4b11-93ac-195d25025b87" />
<img width="1366" height="768" alt="Screenshot 2026-09-29 190301" src="https://github.com/user-attachments/assets/543089b5-ea12-47e7-885e-075878728a1f" />
<img width="1366" height="768" alt="Screenshot 2026-09-29 190613" src="https://github.com/user-attachments/assets/71fcae51-2886-40ce-97d5-69f1a068097b" />
<img width="1366" height="768" alt="Screenshot 2026-09-29 190621" src="https://github.com/user-attachments/assets/26a70a36-7fcb-45df-8a4d-1066818fee7b" />
<img width="1106" height="643" alt="Screenshot 2026-09-29 190410" src="https://github.com/user-attachments/assets/0c6dcac4-2992-4f93-8145-285f687f544e" />
<img width="1366" height="768" alt="Screenshot 2026-09-29 190502" src="https://github.com/user-attachments/assets/4b470cc8-1bb3-4588-b1f0-43240db4877d" />
<img width="1366" height="768" alt="Screenshot 2026-09-29 190518" src="https://github.com/user-attachments/assets/461279d0-084a-4be9-acaa-939c3176e144" />


Add them using:

```markdown id="t8i4qy"
![Login Page](screenshots/login.png)

![Student Dashboard](screenshots/student-dashboard.png)

![Teacher Dashboard](screenshots/teacher-dashboard.png)

![Create Assignment](screenshots/create-assignment.png)
```

---

# 💻 Available Commands

Start development server:

```bash id="t6w9qa"
npm run dev
```

Create production build:

```bash id="q9h8xk"
npm run build
```

Preview production build:

```bash id="g4t2wy"
npm run preview
```

---

# 🌐 Deployment

The application can be deployed using:

* Firebase Hosting
* Vercel
* Netlify

---

# 👩‍💻 Author

**Your Name**

B.Tech — Electronics and Computer Engineering

GitHub:
`https://github.com/YOUR-USERNAME`

LinkedIn:
`https://linkedin.com/in/YOUR-PROFILE`

---

# ⭐ Project Highlights

```text id="5l1c9u"
☁️ Cloud-Based Academic Platform
🔐 Firebase Authentication
🗄️ Cloud Firestore
👨‍🏫 Teacher Dashboard
👨‍🎓 Student Dashboard
📚 Assignment Management
📝 Submission Tracking
⏰ Deadline Management
⚛️ React.js
📱 Responsive UI
🚀 Deployment Ready
```

---

## 📄 License

This project is developed for **educational and portfolio purposes**.
