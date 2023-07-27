# Django Learning Repository

### Setup

```sh
# install with brew
brew install python
# upgrade pip
python3 -m pip install --upgrade pi

# install virtualenv
pip3 install virtualenv
# initiate virtualenv
virtualenv venv
# activate virtualenv

source env/bin/activate
# install django
pip install django

### Create Project

Initiate django project

```sh
django-admin startproject studybud
```

#### Files Generated

`urls.py` - url patterns for the project
`asgi.py` - Asynchronous Server Gateway Interface configuration
`settings.py` - project settings
`wsgi.py` - Web Server Gateway Interface configuration
`manage.py` - command line utility to interact with project


### Run server

```
cd studybud
python manage.py runserver
```

Access the application by going to http://127.0.0.1:8000

### Create an app

An app in django is a module that contains code for models, views, templates, tests, and more. An app can be in multiple projects.

The below will create an app called base

```
python manage.py startapp base
```

This creates a directory called base.

Add the app to the project by adding it to the `INSTALLED_APPS` list in `settings.py`

```python
INSTALLED_APPS = [
    'base.apps.BaseConfig',
    'django.contrib.admin',
    ...
]
```

