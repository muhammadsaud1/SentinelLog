# SentinelLog

A lightweight security event monitoring dashboard built with Flask and PostgreSQL. SentinelLog records successful and failed login attempts, database errors, and source IP addresses, then surfaces them in a single admin view for quick triage.

## Features

- Live security event feed
- INFO, WARNING, and ERROR log levels
- Admin-only dashboard
- Password hashing with bcrypt
- Parameterized SQL queries
- CSRF protection with Flask-WTF
- 15-minute admin session timeout

## Stack

Python · Flask · PostgreSQL (Neon) · HTML · CSS · JavaScript

## Setup

Install the dependencies:

    pip install flask bcrypt pg8000 python-dotenv flask-wtf

Create a `.env` file in the project root with your database connection and Flask secret key:

    DATABASE_URL=your_database_url
    SECRET_KEY=your_secret_key

Create the database tables required by the backend and an admin account with a bcrypt password hash. Start the Flask app and visit `/admin`.

`.env` is git-ignored and must never be committed.

## Project layout

    log_analyzer.py      Flask application and log handling
    templates/           Login, registration, dashboard, admin, notifications
    static/              Stylesheets
