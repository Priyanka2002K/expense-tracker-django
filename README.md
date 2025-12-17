# Expense Tracker API (Django + PostgreSQL)

A simple Expense Tracker web application built using **Python (Django)** and **Django REST Framework**.  
The project provides RESTful CRUD APIs, integrates a third-party API, and includes a reporting feature.

---

## 🚀 Features

- REST API based **CRUD operations** for expenses
- **PostgreSQL** database integration
- **Third-party API integration** (Exchange Rate API example)
- Monthly **expense reporting** (aggregated data)
- Django Admin panel for data management

---

## 🛠️ Tech Stack

- Python 3.x
- Django
- Django REST Framework
- PostgreSQL
- psycopg2
- Requests (for external API calls)

---

## 📁 Project Structure

expense_tracker/
│── config/ # Project settings and URLs
│── expenses/ # Expense app (models, views, serializers)
│── manage.py
│── requirements.txt
│── README.md
---

## ⚙️ Setup Instructions

1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/expense-tracker-django.git
cd expense-tracker-django
2️⃣ Create & Activate Virtual Environmentpython -m venv venv
venv\Scripts\activate      # Windows

3️⃣ Install Dependencies
pip install -r requirements.txt
If requirements.txt is not present:
pip install django djangorestframework psycopg2-binary requests

4️⃣ Configure PostgreSQL Database
expense_tracker_db
Update config/settings.py:
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'expense_tracker_db',
        'USER': 'postgres',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}

5️⃣ Run Migrations
python manage.py makemigrations
python manage.py migrate
6️⃣ Create Admin User
python manage.py createsuperuser
▶️ Run the Application
python manage.py runserver
Open browser:
http://127.0.0.1:8000/
🔑 Admin Panel
http://127.0.0.1:8000/admin/

🔌 API Endpoints
Expense CRUD APIs
Method	Endpoint
GET	/api/expenses/
POST	/api/expenses/
PUT	/api/expenses/{id}/
DELETE	/api/expenses/{id}/
Third-Party API Integration
GET /api/exchange-rate/
Reporting API (Monthly Expense Summary)
GET /api/monthly-report/
🧪 Testing the APIs

You can test APIs using:
Browser
cURL
Example:

curl http://127.0.0.1:8000/api/expenses/
