
pip freeze > requirements.txt

STATIC_ROOT = os.path.join(BASE_DIR, 'static')
Procfile:web: gunicorn myproject.wsgi


pip install gunicorn
pip install django-heroku
import django_heroku
django_heroku.settings(locals())
pip freeze > requirements.txt
git init
git add .
git commit -m "first commit"


heroku login
heroku create myapp --buildpack heroku/python
git push heroku master,main
heroku open

heroku run python manage.py migrate
heroku run python manage.py createsuperuser
