# Django---Installation-Requirements
Documents the setting up of Django dev environment

---

### Setup virtual environment

The following command wil create an environment directory in miniconda3/envs:

`conda create --name` <_Name of the environment_> `python=2.7`

### Create the project

Go to the directory where you want project to be created.

Run the following command to create the project:

`django-admin startproject` <_project name_> 

You will noe see the following two when you run `ls` -- 
**<_project name_>** and **manage.py**

Inside **<_project name_>** you wil see the following files:

  * __init__.py

  * settings.py

  * urls.py

  * wsgi.py

### Setup databases: 

`python manage.py migrate`

Now, you will now see a database there:

**<_project name_>**  **db.sqlite3**  **manage.py**

Finally,

### Run the server

`python manage.py runserver`. Test it by going to http://127.0.0.1:8000/

### Create a new app

`python manage.py startapp browseCatalog`

### validate the models
`python manage.py check`

### Tell django that changes have been made to the model

`python manage.py makemigrations browseCatalog`
