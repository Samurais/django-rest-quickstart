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

### Test REST API with Authentication
* Basic auth
```
GET /example/ HTTP/1.1
Host: 127.0.0.1:8000
Authorization: Basic YWRtaW46cGFzc3dvcmQxMjM=
```

[Generate basic token](https://gist.github.com/Samurais/7f0d9ce24361025a447d7c5ce1adfdc2)

Response
```
{
  "auth": "None",
  "user": "admin"
}
```

Error Response
```
{
  "detail": "Invalid username/password."
}
```