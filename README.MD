DB-GROUP1 – Cloud-Based Django Web Application
Project Overview

This project demonstrates the setup of a cloud-based system on Google Cloud Platform (GCP).
It includes:

A Cloud SQL (MySQL) instance as the database server

A Django web application deployed on Google App Engine (Standard Environment)

1. Prerequisites

Before running or modifying this project, make sure you have:

🐍 Python 3.11+

☁️ Google Cloud SDK (gcloud)

💾 Virtualenv (Python venv)

🔑 Access to the GCP project: db-group1-01

🧠 Optional: Cloud SQL connection info (if database integration is needed later)

2. Clone the Project
git clone https://github.com/your-repo/db-group1.git
cd db-group1

3. Set Up the Virtual Environment
python3 -m venv .venv
source .venv/bin/activate


Then install the dependencies:

pip install -r requirements.txt

4. Project Structure
sql_quizlet/
│
├── mysite/                 # Main Django project
│   ├── settings.py         # Project configuration
│   ├── urls.py             # URL routing
│   └── wsgi.py             # WSGI entry point for Gunicorn
│
├── app.yaml                # Google App Engine configuration
├── requirements.txt        # Python dependencies
├── manage.py               # Django management commands
└── README.md               # This guide

5. Running Locally

You can test the app locally using Django’s development server:

python manage.py runserver


Visit http://127.0.0.1:8000/
 to verify that it’s running.

6. Collect Static Files

Before deployment, make sure to collect all static files:

python manage.py collectstatic --noinput

7. Deploy to Google App Engine

Authenticate your account and select the project:

gcloud auth login
gcloud config set project db-group1-01


Then deploy:

gcloud app deploy


Once deployment finishes, the web app will be available at:
🔗 https://db-group1-01.uw.r.appspot.com

8. Connecting to Cloud SQL (Optional)

If you plan to connect Django to your Cloud SQL (MySQL) instance:

Update DATABASES in mysite/settings.py with the Cloud SQL connection name and credentials.

Install mysqlclient or pymysql as an additional dependency:

pip install mysqlclient


Redeploy after updating settings.

9. Common Commands
Command	Description
python manage.py runserver	Run app locally
python manage.py migrate	Apply database migrations
python manage.py createsuperuser	Create admin account
gcloud app deploy	Deploy app to App Engine
gcloud app browse	Open app in browser