# Info
`manage.py` is a command-line utility that lets you interact with your Django project in various ways. It is especially handy in creating web-apps, managing databases, and most importantly running the server.

Basic syntax for using this utility is `python3 manage.py {command}`

## Usefull commands
### runserver
Runserver is the most important command used with manage.py; It allows you to deploy your website on the server. Django has a wonderful feature that allows you to instantly see changes made on the website without restarting it. (It is only necessary to restart runserver command when adding a new app).

Run this command and navigate to your website with IP given in the outline

If you are willing to run the server to your local network, just add `0.0.0.0:8000` after `runserver` command. (In case if you get an error afterward, just go to settings.py located your websites folder and add this address to ALLOWED_HOSTS as:)
```python
ALLOWED_HOSTS = ['0.0.0.0', '127.0.0.1']
```

### createsuperuser
This command allows you to create an admin account for your Django web admin panel. 

Run this command and access the panel at IP:8000/admin

### startapp
Startapp allows you to initialize an app for your project. Django projects can have infinite number of apps. Basic syntax:

`python3 manage.py startapp {app_name}`

# Setup
Create virtual environment  
`python -m venv venv`

Then activate that environment  
`venv\Scripts\activate`

Then install Django in that environment  
`pip install django`  

Then create django project named mysite  
`django-admin startproject {project_name}`

Now run the following to automatically configure new files.  
`python3 manage.py migrate`   

Run the server with  
`python3 manage.py runserver`

# Links
Django documentation for the intro: [Link](https://docs.djangoproject.com/en/4.0/intro/tutorial01/)  
Guides can be found [here](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django)