# DRFx

A framework for launching new Django Rest Framework projects quickly. Comes with a custom user model, login/logout/signup, social authentication via django-allauth, and more.

## Features

* Django 2.0 and Python 3.6
* Custom user model
* Token-based auth
* Signup/login/logout
* [django-allauth](https://github.com/pennersr/django-allauth) for easy social auth
* [Pipenv](https://github.com/pypa/pipenv) for virtualenvs or Create venv

## First-time setup

1.  Make sure Python 3.6x and Pipenv are already installed. [See here for help](https://djangoforbeginners.com/initial-setup/).
2.  Clone the repo and configure the virtual environment:

```
$ git clone https://github.com/chalermporn/drfx.git
$ cd drfx
$ python -m vnev venv
$ source venv/bin/activate
(venv) pip install -r requirements.txt
```

3.  Set up the initial migration for our custom user models in users and build the database.

```
(venv) $ python manage.py makemigrations users
(venv) $ python manage.py migrate
(venv) $ python manage.py createsuperuser
(venv) $ python manage.py runserver
```

4.  Endpoints

Login with your superuser account. Then navigate to all users. Logout. Sign up for a new account and repeat the login, users, logout flow.

* login - http://127.0.0.1:8000/api/v1/rest-auth/login/
* all users - http://127.0.0.1:8000/api/v1/users
* logout - http://127.0.0.1:8000/api/v1/rest-auth/logout/
* signup - http://127.0.0.1:8000/api/v1/rest-auth/registration/
