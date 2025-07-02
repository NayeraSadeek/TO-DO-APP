# Simple PHP TODO App

This is a simple **Task Management Application** built with **PHP** and **MySQL**.  
You can **add, edit, and delete tasks**, and they appear in a dashboard.

---

## ✨ Features

✅ Add new tasks  
✅ Edit existing tasks  
✅ Delete tasks  
✅ View all tasks in a table  
✅ Success and error messages  
✅ Built with PHP and MySQL  
✅ Bootstrap styling for a clean UI

## 🧩 Requirements
1. PHP 8.1 or newer
2. MySQL 5 or newer
3. DataBase named todolapp and Tables (users,tasks)
4. Web Server (Xampp ,Wamp,Laragon)


## 🛠️ Installation

1. **Clone or download the project folder**
git clone https://github.com/your-username/todo-app.git


2. **Create a MySQL database**

CREATE DATABASE todolapp;

3. **Create the (users) table**
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100)
);

INSERT INTO users (name, email) VALUES ('Tester', 'testing@gmail.com');

4.  **Craete (tasks) table**
CREATE TABLE tasks (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    user_id INT NOT NULL,
    FOREIGN KEY (user_id) REFERENCES users(id)
);

5. **Configure database connection**
$conn = mysqli_connect("localhost:3307", "root", "", "todolapp");

