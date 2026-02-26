# 📝 To-Do App – Architecture Overview

This project is a **Flask-based To-Do Web Application** designed using a clean, modular architecture that separates concerns between routing, business logic, presentation, and data storage.

The application follows a layered design pattern to ensure scalability, maintainability, and future extensibility.

---

## 🏗 Architecture Overview

## 🏗 Architecture Diagram

![To-Do App Python Flask](c:\Users\DELL\Pictures\projrct\To-Do-App-Python-Flask\Blank diagram.png)

The system is structured into the following main layers:

### 1️⃣ Client Layer
- Users interact with the application through a **Web Browser**.
- Communication happens via **HTTP requests**.
- UI is rendered using:
  - HTML
  - CSS
  - Bootstrap
  - Jinja2 templating engine

---

### 2️⃣ Flask Web Application Layer

The core backend is built using **Flask (Python)** and is divided into:

#### 🔹 Task Controller / Routes (CRUD)
- Handles HTTP requests
- Manages Create, Read, Update, Delete operations
- Connects frontend to business logic

#### 🔹 Task Service (Business Logic)
- Processes task-related logic
- Validates inputs
- Manages task transformations
- Separates business rules from route handling

This separation ensures clean code architecture and better maintainability.

---

### 3️⃣ Templates Layer
- Built using **Jinja2 templates**
- Renders dynamic task data
- Styled with HTML/CSS and Bootstrap
- Responsible for UI presentation

---

### 4️⃣ Data Processing Layer
- Uses **Pandas** for data manipulation
- Handles:
  - Task filtering
  - Sorting
  - Data transformations
- Ensures clean separation between logic and storage

---

### 5️⃣ Storage Layer

Current implementation:
- Tasks stored in **CSV / Local file storage**

Future enhancement:
- Replace with relational database (e.g., SQLite or PostgreSQL)

---

## 🔄 Application Flow

1. User sends request from browser  
2. Flask route receives request  
3. Route calls Task Service  
4. Task Service processes logic  
5. Data is read/written to storage  
6. Template renders updated task list  
7. Response sent back to user  

---

## 🚀 Current Features

- Add tasks
- Edit tasks
- Delete tasks
- View task list
- Persistent storage using CSV

---

## 🔮 Planned Future Enhancements

- Multi-list support
- Task categorization / tags
- Sorting & filtering
- Completed task view
- Move tasks between lists
- User authentication
- Database integration

---

## 🧩 Design Principles

- Separation of Concerns  
- Modular Architecture  
- Scalable structure  
- Easy future extensibility  
- Clean CRUD-based routing  

---

## 🛠 Tech Stack

- Python  
- Flask  
- Jinja2  
- HTML/CSS  
- Bootstrap  
- Pandas  
- CSV File Storage  

---

## ▶️ How to Run the Project

```bash
git clone <repository-url>
cd <project-folder>
python -m venv venv
venv\Scripts\activate  # On Windows
pip install -r requirements.txt
python app.py