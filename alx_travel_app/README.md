# ALX Travel App

A Django-based travel application API with JWT authentication.

## Setup Instructions

### Prerequisites

- Python 3.9+
- MySQL Server

### Installation

1. Clone the repository

2. Create and activate a virtual environment:
   ```
   python -m venv venv
   venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

### Database Setup

1. Install MySQL Server if not already installed

2. Create a MySQL database:
   ```
   mysql -u root -p
   CREATE DATABASE alxtravelapp;
   EXIT;
   ```

3. Update the `.env` file with your database credentials if needed

### Running the Application

1. Apply migrations:
   ```
   python manage.py makemigrations
   python manage.py migrate
   ```

2. Create a superuser:
   ```
   python manage.py createsuperuser
   ```

3. Start the development server:
   ```
   python manage.py runserver
   ```

4. Access the API at http://localhost:8000/

## API Endpoints

- `/api/token/` - Obtain JWT token
- `/api/token/refresh/` - Refresh JWT token

## Notes

- For Windows users who encounter issues with mysqlclient installation, you may need to install Microsoft Visual C++ Build Tools. Alternatively, the application is configured to use PyMySQL as a pure Python MySQL client.