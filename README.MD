# SQL Quizlet - Django Web Application

**Live App:** https://db-group1-01.uw.r.appspot.com  
**GitHub Repository:** https://github.com/seecbb007/sqlQuizletgroup1  
**GCP Project ID:** `db-group1-01`

A cloud-based SQL learning platform built with Django and deployed on Google Cloud Platform.

## Quick Start Guide

### Prerequisites
- **Python 3.11 or higher** 
- **Git** 
- **Command Line/Terminal** access

### Step 1: Clone the Repository

Open your terminal/command prompt and run:

```bash
# Clone the repository
git clone https://github.com/seecbb007/sqlQuizletgroup1.git

# Navigate to the project directory
cd sqlQuizletgroup1
```

### Step 2: Set Up Python Virtual Environment

```bash
# Create a virtual environment
python3 -m venv venv

# Activate the virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
# Install required packages
pip install -r requirements.txt
```

### Step 4: Run Database Migrations

```bash
# Apply database migrations
python manage.py migrate
```

### Step 5: Start the Development Server

```bash
# Start the Django development server
python manage.py runserver
```

### Step 6: Access the Application

Open your web browser and go to: **http://127.0.0.1:8000/**

You should see the SQL Quizlet application running locally!

---

## 📁 Project Structure

```
sql_quizlet/
├── mysite/                 # Django project settings
│   ├── __init__.py
│   ├── settings.py         # Django configuration
│   ├── urls.py            # URL routing
│   └── wsgi.py            # WSGI configuration
├── staticfiles/           # Static files (CSS, JS, images)
├── app.yaml               # Google App Engine configuration
├── requirements.txt       # Python dependencies
├── manage.py              # Django management script
├── db.sqlite3            # SQLite database (local development)
└── README.md             # This file
```

---

## 🛠️ Development Commands

### Basic Django Commands

```bash
# Start development server
python manage.py runserver

# Create database migrations
python manage.py makemigrations

# Apply database migrations
python manage.py migrate

# Create a superuser (admin account)
python manage.py createsuperuser

# Collect static files (for deployment)
python manage.py collectstatic --noinput
```

### Virtual Environment Commands

```bash
# Activate virtual environment
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# Deactivate virtual environment
deactivate
```

---

## 🌐 Deployment to Google App Engine

### Prerequisites for Deployment
- Google Cloud SDK installed ([Download here](https://cloud.google.com/sdk/docs/install))
- Access to the GCP project `db-group1-01`

### Deploy Commands

```bash
# Authenticate with Google Cloud
gcloud auth login

# Set the project
gcloud config set project db-group1-01

# Collect static files
python manage.py collectstatic --noinput

# Deploy to App Engine
gcloud app deploy

# Open the deployed app
gcloud app browse
```

---

## 📋 Requirements

The project uses the following main dependencies:

- **Django 4.2.25** - Web framework
- **Gunicorn 23.0.0** - WSGI server for production
- **WhiteNoise 6.11.0** - Static file serving

See `requirements.txt` for the complete list.


---

## 🔄 Next Steps

This project is currently in **Phase III** of development:
- ✅ Django web application setup
- ✅ Google App Engine deployment
- 🔄 Cloud SQL integration (coming next)
- 🔄 Advanced SQL quiz features

---






