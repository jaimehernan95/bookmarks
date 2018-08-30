Building a Social Website
Objectives:
1. Creating a social website project
2. Using the Django authentication framework
3. Password Authentication
4. User Registration and User Profiles
5. Building a customer authentication backend
6. Adding Social Authentication to your site

requirements:
Django 1.8
Python3
DB Postgres
System OS High Sierra
Pycharm CE basic or Atom


Creating a Social Website Project

• Creating a social application that will allow users to shares images they find on the
internet
• Create a virtual environment for your project and activate it
• Create the initial project structure
Building Elements for creating a social website
• Users to register, log in, edit profile, and reset their password
• Allow users to follow each other
• Display shared Images
• Allow Users to see the content uploaded by the people

Open the terminal and create virtual environment
 ~ $ pip3 install virtualenv
Installing setuptools, pip, wheel…done.


Activate virtual environment
$ source ~/vir_proj_dir/bin/activate
Install Django
(vir_proj_dir) ikueJaime ~ $ pip3 install Django==1.8.6
Collecting Django==1.8.6
Using cached https://files.pythonhosted.org/packages/d2/8b/
115baec29ab28754da734b89e4a6aa8e5f0588d1b8f0db03d8b9f87bb88c/Django-1.8.6-
py2.py3-none-any.whl
Installing collected packages: Django
Successfully installed Django-1.8.6


Create bookmarks project
(vir_proj_dir) ikueJaime ~ $ django-admin startproject bookmarks
(vir_proj_dir) ikueJaime ~ $ cd bookmarks
(
(vir_proj_dir) ikueJaime ~/bookmarks $ django-admin startapp account
(vir_proj_dir) ikueJaime ~/bookmarks $ ls
total 24
drwxr-xr-x 7 staff 238B Jun 13 23:08 ./
drwxr-xr-x@ 80 staff 2.7K Jun 13 23:07 ../
-rw-r--r--@ 1 staff 6.0K Jun 13 23:08 .DS_Store
drwxr-xr-x 3 staff 102B Jun 13 23:08 .idea/
drwxr-xr-x 8 staff 272B Jun 13 23:06 account/
drwxr-xr-x 6 staff 204B Jun 13 23:05 bookmarks/
-rwxr-xr-x 1 staff 252B Jun 13 23:05 manage.py*

Migrate Database

(vir_proj_dir) ikueJaime ~/bookmarks $ python3 manage.py migrate
Operations to perform:
Synchronize unmigrated apps: staticfiles, messages
Apply all migrations: auth, contenttypes, sessions, admin
Synchronizing apps without migrations:
Creating tables...
Running deferred SQL...
Installing custom SQL...
Running migrations:
Rendering model states... DONE
Applying contenttypes.0001_initial... OK
Applying auth.0001_initial... OK
Applying admin.0001_initial... OK
Applying contenttypes.0002_remove_content_type_name... OK
Applying auth.0002_alter_permission_name_max_length... OK
Applying auth.0003_alter_user_email_max_length... OK
Applying auth.0004_alter_user_username_opts... OK
Applying auth.0005_alter_user_last_login_null... OK
Applying auth.0006_require_contenttypes_0002... OK
Applying sessions.0001_initial... OK



Create a super user ADMIN

go to bookmarks and create super user
(vir_proj_dir) ikueJaime ~ $ cd ~/bookmarks
(vir_proj_dir) ikueJaime ~/bookmarks $ python3 manage.py createsuperuser
Username (leave blank to use 'ikuejaime'): admin
Email address: your-email@gmail.com
Password:
Password (again):
Superuser created successfully.


Run Server

(vir_proj_dir) ikueJaime ~/bookmarks $ python3 manage.py runserver
Performing system checks...
System check identified no issues (0 silenced).
June 16, 2018 - 06:41:57
Django version 1.8.6, using settings 'bookmarks.settings'

