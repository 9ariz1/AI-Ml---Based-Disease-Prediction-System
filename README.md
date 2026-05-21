# Disease Prediction System (DPS) - Django Project

A machine learning based Disease Prediction System built using Django, Python, Pandas, and Joblib. This project predicts diseases based on user symptoms and stores prediction history in a database.

---

## Features

- Predict disease using symptoms input
- Machine Learning model integration (`best_model.pkl`)
- CSV file prediction support
- Prediction history storage
- Django-based web interface
- SQLite database support

---

## Tech Stack

- Python
- Django
- Pandas
- Scikit-learn
- Joblib
- HTML/CSS
- SQLite3

---

## Project Structure

```bash
DPS Django/
│
├── dp_project/
│   ├── manage.py
│   ├── db.sqlite3
│   │
│   ├── dp_project/
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── wsgi.py
│   │   └── asgi.py
│   │
│   └── dpapp/
│       ├── views.py
│       ├── models.py
│       ├── admin.py
│       ├── best_model.pkl
│       ├── label_encoder.pkl
│       ├── templates/
│       ├── static/
│       └── migrations/
```

---

## Installation Guide

### 1. Clone Repository

```bash
git clone <your-repository-link>
cd "DPS Django"
```

### 2. Create Virtual Environment

```bash
python -m venv venv
```

### 3. Activate Virtual Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux/Mac

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install django pandas scikit-learn joblib
```

---

## Run Project

Move to project directory:

```bash
cd dp_project
```

Run migrations:

```bash
python manage.py migrate
```

Start server:

```bash
python manage.py runserver
```

Open browser:

```bash
http://127.0.0.1:8000/
```

---

## Disease Prediction Inputs

The model uses the following symptoms:

- Fever
- Headache
- Nausea
- Vomiting
- Fatigue
- Joint Pain
- Skin Rash
- Cough
- Weight Loss
- Yellow Eyes

---

## Machine Learning Integration

The project loads:

- `best_model.pkl` → Trained ML model
- `label_encoder.pkl` → Encoded disease labels

Prediction flow:

1. User enters symptoms
2. Data converted into DataFrame
3. Model predicts disease
4. Encoded label converted to disease name
5. Result stored in database history

---

## CSV Prediction Feature

Users can upload a CSV file for disease prediction.

Expected CSV format:

```csv
fever,headache,nausea,vomiting,fatigue,joint_pain,skin_rash,cough,weight_loss,yellow_eyes,disease
1,0,1,0,1,0,0,1,0,0,Unknown
```

---

## Database

SQLite database is used by default.

Database file:

```bash
db.sqlite3
```

---

## Future Improvements

- User authentication system
- Multiple disease predictions
- Better UI/UX design
- Deploy on Render or Heroku
- Add API support
- Use larger medical datasets

---

## Author

**Mo Ariz**

- Python Developer
- Data Science Enthusiast

LinkedIn: https://www.linkedin.com/in/mo-ariz/

---

## License

This project is for educational and learning purposes.
