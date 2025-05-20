# Django-DRF-JWT-Install

## Install
- Django
- Django REST Framework
- JWT Authentication


## Setup Instructions

###  Create and enter your project folder

```bash
python3 -m venv env

# Then activate the virtual environment
source env/bin/activate
```

###  Install Django, DRF, and JWT

```bash
pip install django djangorestframework djangorestframework-simplejwt
```

### Start your Django project and app

```bash
# Django Project
django-admin startproject employer_system .

# Django Project App
python manage.py startapp employe
```

### Inside YourProject/settings.py, add these changes:

```bash
INSTALLED_APPS = [
    ...
    'rest_framework',
    'rest_framework_simplejwt',
    'employe',
]

# Add REST Framework config:
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': (
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ),
}

```

### Apply initial migrations

```bash
python manage.py migrate
```

### Create superuser

```bash
python manage.py createsuperuser
```

### Run and Check

```bash
python manage.py runserver
```
