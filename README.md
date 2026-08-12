# Dev Journal

A full-stack web app for tracking what you're learning as a developer — log topics like languages, frameworks, or algorithms, and journal your progress on each one as you go.

Built this to have a running record of my own learning path (Python, Java, DSA) instead of scattered notes — small, but it's genuinely part of how I track my own study now.

**Live demo:** [https://dev-journal-m4o2.onrender.com](https://dev-journal-m4o2.onrender.com)

## Features

- **User authentication** — register, log in, log out
- **Topic management** — create, edit, and delete topics you're learning about (languages, frameworks, algorithms, whatever you're studying)
- **Entry tracking** — add multiple journal entries per topic to log progress over time
- **Private by default** — topics and entries are only visible to the user who created them

## Tech stack

- **Backend:** Python, Django 4.2
- **Frontend:** HTML, CSS, Bootstrap 3
- **Database:** PostgreSQL (SQLite for local development)
- **Deployment:** Render, with WhiteNoise for static file serving

## Running it locally

```bash
git clone https://github.com/turganaliev/dev-journal.git
cd dev-journal

python3 -m venv env
source env/bin/activate      # Windows: env\Scripts\activate

pip install -r requirements.txt
```

Create a `.env` file in the project root:
```
SECRET_KEY=local-secret-key
DEBUG=True
ALLOWED_HOSTS=127.0.0.1,localhost
```

Generate a secret key with:
```bash
python3 -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
```

Then run migrations and start the server:
```bash
python3 manage.py migrate
python3 manage.py runserver
```
Visit `http://127.0.0.1:8000`.

## Deployment

Deployed on Render with a managed PostgreSQL instance. Environment variables (`SECRET_KEY`, `DEBUG`, `ALLOWED_HOSTS`, `DATABASE_URL`) are configured in the Render dashboard rather than committed to the repo.
