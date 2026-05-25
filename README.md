# Task Master - Flask CRUD To-Do App

Task Master is a simple Flask web application that allows users to create, view, update, and delete tasks.  
It is built as a beginner-friendly CRUD project using Flask, Flask-SQLAlchemy, SQLite, HTML, CSS, and Jinja2 templates.

---

## Features

- Add a new task
- View all tasks in a table
- Update an existing task
- Delete a task
- Store tasks in a SQLite database
- Use Flask templates with Jinja2
- Use static CSS for styling
- Ready for deployment on Heroku

---

## Technologies Used

- Python 3
- Flask
- Flask-SQLAlchemy
- SQLite
- HTML
- CSS
- Jinja2
- Gunicorn
- Git and GitHub
- Heroku

---

---

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Imranay/Todo-Task-Manager
cd Todo-Task-Manager
```

### 2. Create a Virtual Environment

For Windows:

```bash
python -m venv env
```

For Mac/Linux:

```bash
python3 -m venv env
```

### 3. Activate the Virtual Environment

For Windows:

```bash
env\Scripts\activate
```

For Mac/Linux:

```bash
source env/bin/activate
```

### 4. Install Required Packages

```bash
pip install -r requirements.txt
```

Or install packages manually:

```bash
pip install flask flask-sqlalchemy gunicorn
```

'''

## Database Setup

Open Python shell:

```bash
python
```

Then run:

```python
from app import app, db

with app.app_context():
    db.create_all()
exit()
```

This will create the SQLite database file:

```text
test.db
```

---

## Run the Application

```bash
python app.py
```

Now open this URL in your browser:

```text
http://127.0.0.1:5000/
```

or

```text
http://localhost:5000/
```

---

## Main Routes

| Route | Method | Purpose |
|---|---|---|
| `/` | GET | Show all tasks |
| `/` | POST | Add a new task |
| `/update/<id>` | GET | Show update page |
| `/update/<id>` | POST | Update selected task |
| `/delete/<id>` | GET | Delete selected task |

---

## CRUD Operations

| CRUD | Meaning | In This App |
|---|---|---|
| Create | Add data | Add a new task |
| Read | View data | Show all tasks |
| Update | Edit data | Update task content |
| Delete | Remove data | Delete a task |

---

---

## Heroku Deployment

### 1. Install Gunicorn

```bash
pip install gunicorn
```

### 2. Create `requirements.txt`

```bash
pip freeze > requirements.txt
```

### 3. Create `Procfile`

Create a file named `Procfile` with no extension.

Inside it write:

```text
web: gunicorn app:app
```

### 4. Login to Heroku

```bash
heroku login
```

### 5. Create Heroku App

```bash
heroku create your-app-name (all small letters)
```

### 6. Push to Heroku

```bash
git push heroku main
```

If your branch is named `master`, use:

```bash
git push heroku master
```

'''
## Author

Created as a beginner Flask CRUD project for learning web development with Python.
