📦 Dockerized Flask + MySQL + HTML Form

This project demonstrates a simple Flask web app with an HTML form connected to a MySQL database, all running inside Docker containers using Docker Compose.

It is a beginner-friendly DevOps project to understand:

How to use Docker for multi-container apps

How to connect a Flask web app with MySQL

How to interact with a database using a web form

🚀 Features

HTML form page to enter user information

Flask backend to process form submissions

MySQL database for storing user data

Docker Compose setup for running Flask + MySQL

📂 Project Structure
.
├── app.py                # Flask backend logic
├── templates/            # HTML frontend form
│   └── index.html
├── requirements.txt      # Python dependencies
├── Dockerfile            # Flask container build file
├── docker-compose.yml    # Multi-container setup
└── README.md             # Project documentation

🛠️ Setup Instructions

Start the Containers
docker-compose up -d

Create Database & Table

Enter the MySQL container:

docker exec -it docker-db-1 mysql -u root -p


Inside MySQL:

CREATE DATABASE flaskdb;
USE flaskdb;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100)
);

🌐 Usage

Open in browser:

http://localhost:5000


Enter a name in the HTML form and submit.

The submitted data will be stored inside MySQL container.

To view data:

docker exec -it docker-db-1 mysql -u root -p flaskdb
SELECT * FROM users;

📖 Key Learnings

Running multiple containers with Docker Compose

Connecting Flask backend with MySQL

Building a web interface (HTML form) for database input

Using Docker to simulate a real-world app setups