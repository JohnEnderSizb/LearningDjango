# LearningDjango
Code for the Youtube Django tutorial: https://youtu.be/JT80XhYJdBw (Python Django Tutorial 2020 - Full Course for Beginners)


# **NOTES**



# CREATE VIRTUAL ENV

* ``` python3 -m venv --system-site-packages ./venv ```

## ACTIVATE VIRTUAL ENV

* ``` source ./venv/bin/activate  # sh, bash, or zsh ```

## THEN

* ``` pip install --upgrade pip ```
* ``` pip list  # show packages installed within the virtual environment ```
* ``` deactivate  # don't exit until you're done ```

# INSTALL DJANGO

* ```python -m pip install Django```

# START PROJECT

* ```django-admin startproject mysite```

# RUN SERVER

* ``` python manage.py runserver  # inside your project directory ```

# CREATE AN APP

* Make sure you are in the same level as manage.py
* Your apps can live anywhere on your Python path. In this tutorial, we’ll create our poll app in the same directory as your manage.py file so that it can be imported as its own top-level module, rather than a submodule of mysite.
* ``` manage.py startapp polls```

# MIGRATE DATABASE
* ```python manage.py migrate```
* Models have to be activated in settings

## RUNNING MIGRATIONS

* ```python manage.py makemigrations polls``` 
* To see the SQL: ```python manage.py sqlmigrate polls 0001```
* After making migrations, comit them by:  ```python manage.py migrate```

# PLAYING WITH THE API

* Acticate the shell: ```python manage.py shell```
* We’re using this instead of simply typing “python”, because manage.py sets the DJANGO_SETTINGS_MODULE environment variable, which gives Django the Python import path to your mysite/settings.py file.
* Once you’re in the shell, explore the database API:
* ```from polls.models import Choice, Question  # Import the model classes we just wrote```
* diff between get and filter
