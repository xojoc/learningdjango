# What is *learningdjango*?

I use this project to experiment and try out the features of Django and its ecosystem.
This project uses the following stack:

   - [Django](https://www.djangoproject.com/)
   - [Celery](http://www.celeryproject.org/)
   - [Redis](https://redis.io/)
   - [Poetry](https://python-poetry.org/)
    
I also use it as the base for my tutorials and articles on [my blog](https://xojoc.pw/blog/).

# Steps to recreate the project from scratch

Create a new directory and switch to it
```shell script
mkdir learningdjango
cd learningdjango
```

[install Poetry](https://python-poetry.org/docs/#installation) and init a new project by creating the `pyproject.toml` file
with `Django` as a dependency
```shell script
poetry init --no-interaction --dependency django
```
to add other dependencies later on, just run `poetry add` like so
```shell script
poetry add celery
```
then create the virtual environment with all the dependencies
```shell script
poetry install
```

and create a new Django project in the current directory
```shell script
poetry run django-admin.py startproject learningdjango .
```

finally run the migrations for the default apps and [run the development web server](https://docs.djangoproject.com/en/dev/ref/django-admin/#runserver)
```shell script
poetry run python3 manage.py migrate
poetry run python3 manage.py runserver 7000
```

Go to [localhost:7000](http://localhost:7000) and you should see the default Django page...

# Who?

*learningdjango* was written by [Alexandru Cojocaru](https://xojoc.pw).

# License

[AGPLv3](https://www.gnu.org/licenses/agpl-3.0.en.html) or later.

