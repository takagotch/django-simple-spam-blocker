### django-simple-spam-blocker
---
https://github.com/moqada/django-simple-spam-blocker

```py
INSTALLED_APPS = (
  'simplespamblocker',
)

MIDDLEWARE_CLASSES = (
  'simplespamblocker.middleware.SpamBlockMiddleware',
)

SIMPLESPAMBLOCKER_PROFILES = (
  (r'^/comments/post/$', {
    'method': 'post',
    'author': lambda request: request.POST.get('name', ''),
    'email': lambda request: request.POST.get('email', ''),
    'url': lambda request: request.POST.get('url', '),
    'content': lambda request: request.POST.get('comment', ''),
  }),
)


```

```sh
python manage.py syncdb
python manage.py migrate simplespamblocker
```

```
```


