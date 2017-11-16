# Django---Installation-Requirements
Documents the setting up of Django dev environment


### Set up virtual environment

The following command wil create an environment directory in miniconda3/envs:

`conda create --name` <_Name of the environment_> `python=2.7`

go to the directory where you want project to be created.

Run the following command to create the project:

`django-admin startproject` <_project name_> 

You will noe see the following two when you run `ls` -- 
**<_project name_>** and **manage.py**

Inside **<_project name_>** you wil see the following:

__init__.py

settings.py

urls.py

wsgi.py

Run the folowing command to setup databases: 

`python manage.py migrate`

You will now also see **db.sqlite3** :

**<_project name_>**  **db.sqlite3**  **manage.py**
