# Qualitative-Polls-Django-App
A user polls app for Django projects that uses Javascript/JQuery/AJAX to create, serve, and receive user polls that allow text area information. By Okasen on Github, AKA Jennifer Black, AKA @JenniLBlack on Twitter. App is offered without warranty of any kind.

REQUIREMENTS:
Python - this is a python app, so you need the interpreter

Django - this is an app to work in an existing Django project. It can be installed in almost any app that satisfies the following requirements:

--JQuery - you must have the JQuery source saved as a .js file and point the script in base.html to your JQuery.js file. Keeping JQuery.js in the base static folder works

--a "user"/"accounts" app. The polls require a user ID to be assigned to each answer (this is not anonymous polling, but it could be changed to be)

--the users must include staff users, OR you must alter the code to remove the "UserPassesTestMixin" from QAView. (this mixin prevents non-authorized users from creating and deleting questions)

TO INSTALL:
NOTE: Install instructions are a work in progress at the current moment-- I still need to test them on a fresh Django project
-1--Clone the repo to a folder named "user_polls" in your Django app directory

-2--Identify the name of your main User model, or create a user/accounts app that will supply the model

-2a-In the default app, the user model is called "Player". So, anywhere you see the word Player, replace it with your User model's name.

-2b-The locations where player is used are: TBA

-3--place user_polls in your installed apps section of settings.py

-4--add the following line to your urls.py in your main app: path('polls/', include('user_polls.urls')),

-5--run manage.py makemigrations and then manage.py migrate to create the databases for questions and answers

-6-optional but recommended: Run manage.py tests. There is a test file included with a few tests that should indicate whether your app installed properly
