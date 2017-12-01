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

### The sqlmigrate command takes migration names and returns their SQL

`python manage.py sqlmigrate browseCatalog 0001`

The sqlmigrate command doesn’t actually create the tables or otherwise touch your database – it just prints output to the screen so you can see what SQL Django would execute if you asked it.

###  committing the SQL to the database

`python manage.py migrate`


### Object initialization and saving it
```
p1 = Publisher(...)
# At this point, p1 is not saved to the database yet!
p1.save()
# Now it is.
```

If you want to create an object and save it to the database in a single step, use the objects.create() method.
