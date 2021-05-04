# GraphQL-Python
Python implementation of a GraphQL server

## 0. Setup
```
 python3 -m venv .
 source bin/activate
 python3 -m pip install --upgrade pip
 pip install django==2.1.4 graphene-django==2.2.0 django-filter==2.0.0 django-graphql-jwt==0.1.5
 django-admin startproject hackernews
 cd hackernews
 python manage.py migrate
 python manage.py runserver
```

### Edit `hackernews/settings.py`
```
INSTALLED_APPS = (
    # After the default packages
    'graphene_django',
)

...
GRAPHENE = {
    'SCHEMA': 'hackernews.schema.schema',
}
```

### Run
```
 python manage.py runserver
```
### Go to `http://localhost:8000`
Django's "hello" page is displayed!

