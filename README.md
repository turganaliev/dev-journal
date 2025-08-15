# Learning Log App

This is a full-stack web application built with Python and Django. The app is designed to help users keep a personal record of topics they are learning about, as well as journal entries related to those topics.

## Features

* **User Authentication:** Users can register, log in, and log out.
* **Topic Management:** Logged-in users can create, edit, and delete topics.
* **Entry Tracking:** Users can add multiple entries to each topic.
* **Private Data:** All topics and entries are private and accessible only to the user who created them.

## Technologies Used

* **Back-End:** Python, Django
* **Front-End:** HTML, CSS
* **Database:** SQLite (default for development)
* **Hosting:** PythonAnywhere

## Getting Started

To run this project locally, follow these steps:

1.  Clone the repository:
    ```bash
    git clone [https://github.com/turganaliev/web_app.git](https://github.com/turganaliev/web_app.git)
    cd web_app
    ```
2.  Set up a virtual environment and install dependencies:
    ```bash
    python -m venv venv
    source venv/bin/activate
    pip install -r requirements.txt
    ```
    *(Note: You will need to create a `requirements.txt` file by running `pip freeze > requirements.txt`.)*
3.  Apply database migrations and run the server:
    ```bash
    python manage.py makemigrations learning_logs
    python manage.py migrate
    python manage.py runserver
    ```

## Live Demo

You can view a live version of the application here:
[https://turganaliev.pythonanywhere.com/](https://turganaliev.pythonanywhere.com/)
