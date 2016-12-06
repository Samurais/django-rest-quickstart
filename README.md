# django-rest-quickstart
Built with [django-rest-framework](http://www.django-rest-framework.org/tutorial/quickstart/)

## Launch
```
pip install django djangorestframework 
cd app
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser # create a user, e.g. admin:password123
python manage.py runserver
```

## Login admin panel
```
open http://127.0.0.1:8000/admin/login/?next=/admin/
```
Fill in admin: password123


## Test REST API
```
GET /users/ HTTP/1.1
Host: 127.0.0.1:8000
Content-Type: application/json
```

Response
```
[
  {
    "url": "http://127.0.0.1:8000/users/1/",
    "username": "admin",
    "email": "",
    "groups": []
  }
]
```