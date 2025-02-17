# Bubble Game Web Application

This repository contains a **Flask-based Bubble Game Web Application** with user authentication using MySQL. Users can **sign up, log in, and play the game**. The game interface is built using **HTML, CSS, and JavaScript**, while the backend is powered by **Flask and MySQL**.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Environment Variables](#environment-variables)
- [API Routes](#api-routes)
- [Database](#database)
- [Frontend](#frontend)
- [License](#license)

## Features

- **User Authentication:** Signup & Signin with bcrypt password hashing.
- **Game Pages:** Different pages for home, game entry, and gameplay.
- **Flask & MySQL Integration:** Stores user details in MySQL database.
- **Flask-WTF Forms:** Secure form handling with validation.
- **Frontend Design:** Built using HTML, CSS, and JavaScript for an interactive experience.

## Installation

### Prerequisites
- Python 3.x
- MySQL Database
- Virtual Environment (Recommended)
- Node.js (For additional frontend enhancements, if applicable)

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/bubble-game.git
   cd bubble-game
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up MySQL Database:**
   ```sql
   CREATE DATABASE bubble_game;
   USE bubble_game;
   CREATE TABLE users (
       id INT AUTO_INCREMENT PRIMARY KEY,
       username VARCHAR(100) NOT NULL,
       email VARCHAR(100) UNIQUE NOT NULL,
       password VARCHAR(255) NOT NULL
   );
   ```

5. **Configure environment variables:** (See [Environment Variables](#environment-variables))

6. **Run the application:**
   ```bash
   python app.py
   ```

## Environment Variables

Set the following environment variables in a `.env` file or export them:
```plaintext
MYSQL_HOST=localhost
MYSQL_USER=root
MYSQL_PASSWORD=yourpassword
MYSQL_DB=bubble_game
SECRET_KEY=your_secret_key
PORT=5000
```

## API Routes

### Public Routes
- `GET /` → Home page
- `GET /enter` → Game entry page
- `GET /game` → Bubble game page

### Authentication Routes
- `GET, POST /signup` → User signup
- `GET, POST /signin` → User signin

## Database
- Uses **MySQL** as the database.
- Stores user credentials securely with **bcrypt hashing**.
- Uses Flask-MySQLdb for database interactions.

## Frontend
- The game interface is built using **HTML, CSS, and JavaScript**.
- Uses **Flask templates (Jinja2)** for rendering dynamic content.
- JavaScript handles game mechanics and user interactions.
- CSS ensures responsive and visually appealing UI.


Feel free to contribute or raise issues for improvements! 🎮🚀

