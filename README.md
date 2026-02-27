# Task Management App


## 2.1.3.1 Overview of what is being built  

This is a simple Task Management CRUD application where users can create, read, update, delete and search tasks.  
The project is built using React (Vite) for frontend, Express.js for backend, and Supabase (PostgreSQL) as the database.  

The goal of this project is to demonstrate full-stack development using proper structure and clean separation between client and server.

---

## 2.1.3.2 Explanation of DB Design  

The database is hosted on Supabase (PostgreSQL).  

There is one main table called **tasks** which stores:
id
task_title
task_description
task_due_date
task_status
task_remarks
created_on
last_updated_on
created_by_name
created_by_id
last_updated_by_name
last_updated_by_id

Indexes are added on commonly searched fields like status, due date and title for better performance.  


---

## 2.1.3.3 Structure of the Application  

The project is divided into two folders:

- **client** → Frontend (React + Vite)  
- **server** → Backend (Express.js - MVC pattern)  

### 2.1.3.3.1 SPA Approach  

This project uses a **Single Page Application (SPA)** approach.  

The React frontend communicates with the Express backend using REST APIs.  
The backend handles all database operations and sends JSON responses to the frontend.  

MVC pattern is followed inside the backend:
- Routes → define endpoints  
- Controllers → handle request/response  
- Models → interact with Supabase database  

---

## 2.1.3.4 Frontend Structure  

### 2.1.3.4.1 What frontend is used and why?  

React (with Vite) is used as the frontend because it allows fast development, reusable components and smooth user experience without page reloads.  

It is a web-based frontend (not mobile app).  

The SPA structure makes the UI responsive and dynamic while interacting with backend APIs.

---

## 2.1.3.5 Build and Install  

### 2.1.3.5.1 Environment details and dependencies  

Backend dependencies:
- express  
- cors  
- @supabase/supabase-js  
- dotenv  

Frontend:
- React  
- Vite  

There are two `.env` files:
- Root `.env` (used by server)  
- `client/.env` (used by frontend)  

For easier testing of this assessment, I have temporarily included my personal `.env` file in the repository (I understand this is not safe in production).

---

### 2.1.3.5.2 How to build the project  

Simply run:

npm run build  

This installs dependencies for both server and client and builds the frontend.

---

### 2.1.3.5.3 How to run the project  

Clone the repository and run:

cd server  
npm install
npm run dev  

Open a new terminal and from root folder run:
npm install
npm run dev  

Then open the browser and test the application.

---