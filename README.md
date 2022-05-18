# Python - Django Blog

    []: # Language: markdown
    []: # Path: README.md

__Running the Django Blog__
python manage.py runserver

python manage.py startapp blog


__Deploy the Django Blog__

1. pip install gunicorn
2. pip install django-heroku
3. pip install dj_database_url
4. pip install python-decouple
5. touch Profile -> _web: gunicorn __appname__.wsgi_ #django_blog
6. pip freeze > requirements.txt
7. add __import django_heroku, dj_database_url__ to __settings.py__
8. add __from decouple import config__ to __settings.py__
9. add __STATICFILES_STORAGE = ['whitenoise.storage.CompressedManifestStaticFilesStorage']__ to __settings.py__
10. add __django_heroku.settings(locals())__ to __settings.py__