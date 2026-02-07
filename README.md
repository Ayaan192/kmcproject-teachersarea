# 🎓 KMC School Management Portal  
## Real-Time School Management System for KMC school

---

## 📖 Project Overview

The **KMC School Management Portal** is a real-time, cloud-based school web application designed to improve communication between **teachers, students, and parents**.

The system ensures that academic information such as **homework, notices, attendance, timetables, and feedback** is updated instantly without requiring manual page refreshes.

The project is built using **HTML, CSS, JavaScript, and Firebase Realtime Database**, following a clean and modular architecture suitable for educational environments.

---

## 🏫 System Architecture Overview

The portal is divided into **two distinct ecosystems**, connected through a **central cloud database**:

1. **Administrative Engine (Teacher Area)** – Data Creation & Management  
2. **Information Hub (Student Area)** – Data Viewing & Interaction  

Firebase acts as the **single source of truth**, enabling real-time synchronization between all modules.

---

## 👨‍🏫 1. Teacher Area –

The **Teacher Area** is the control center of the system.  
All academic data is **created, updated, and managed** here.

### Key Characteristics
- Full write and management access
- Real-time data publishing

### Teacher Pages & Functions

| Page Name | File Name | Description |
|---------|----------|-------------|
| Teachers login | `teacher-login.html` | Secure login page for teachers |
| Teachers Dashboard | `dashboard.html` | Central navigation hub |
| Attendance page | `attendance.html` | Mark students Present/Absent |
| Notice Creator | `notice-up.html` | Create and publish notices |
| Homework uploader | `teacher-homework.html` | Upload homework with deadlines |
| Routine viewer | `timetable.html` | Manage class timetable |
| Task manager | `todo.html` | Teacher personal task manager |
| Feedback giver | `teacher-feedback.html` | View parent complaints |

All actions in this area **write data directly to Firebase**, making updates instantly available to students.

---

## 🎓 2. Student Area –

The **Student Area** is designed for viewing academic content and communicating with teachers.

### Key Characteristics
- Read-only access to academic data
- Simple and student-friendly interface
- Real-time automatic updates

### Student Pages & Functions

| Page Name | File Name | Description |
|---------|----------|-------------|
| Student Gateway | `student-login.html` | Student login page |
| Personal Hub | `student-dashboard.html` | Student home dashboard |
| Homework Feed | `student-homework.html` | View assigned homework |
| Live Notice Board | `student-notice.html` | View school notices |
| Timetable | `student-timetable.html` | View daily timetable |
| Communication Module | `parents-complain.html` | Parents send messages |

Students **do not modify data**.  
They only consume verified information provided by teachers.

---

## 🔄 3. Data Synchronization Workflow 

This is the **core logic** of the project.

### Step-by-Step Flow

1. **Teacher Input**  
   Teacher submits data (homework, notice, attendance, timetable).

2. **Firebase**  
   Data is stored in Firebase Realtime Database.

3. **Real-Time Sync**  
   Student pages use Firebase listeners that detect changes instantly.

4. **Instant UI Update**  
   Student pages update automatically show data if teacher enter.

5. **Feedback**  
   Parents send complaints via student portal →  
   Messages appear in teacher feedback inbox.

---

## 🛠 Technologies Used

| Layer | Technology |
|-----|-----------|
| Frontend | HTML5, CSS3, JavaScript |
| Backend | Firebase Realtime Database |
| Hosting | Github page and Netlify |

---

## 🏗 Project Structure

```plaintext
/kmc-school-portal
│
├── index.html
│
├── teacher-login.html
├── dashboard.html
├── attendance.html
├── notice-up.html
├── teacher-homework.html
├── timetable.html
├── todo.html
├── teacher-feedback.html
│
├── student-login.html
├── student-dashboard.html
├── student-homework.html
├── student-notice.html
├── student-timetable.html
├── parents-complain.html
│
├── style.css
├── dashboard.css
├── attendance.css
├── notice.css
├── notice-up.css
├── timetable.css
├── todo.css
├── teacher-homework.css
├── student-dashboard.css
├── student-homework.css
├── student-notice.css
├── student-timetable.css
├── parents-complain.css
├── teacher-feedback.css
│
├── kmc logo.png
├── wireframe.png
├── workflow.png
