Secure User Login System with Flask and SQL Alchemy




Step 1: Set up Virtual Environment
    - Use command python3 -m venv (name environment)
    - Use command source (enviromentname/bin/activate)
    - Use command deactivate to turn of virtual environment
    - Install Pip3, Flask and Flask_SQLAchemy
    - Run pip freeze > requirments.txt to see all liberies needed
    - Open a 'main.py' 'index.html', 'base.html', dashboard.html file, a 'static' and 'templates' folders

Step 2: Setting Up The Project 
    - Import all needed liberies from Flask, render_templates, request, redirect, session, url_for
    - Create an app object from the flask class 'app = Flask__name__'
    _ Set to run from the mail page 'if __name__ in "__main__": app.run(debug=True)'
    - Create and defind an app route '@app.route("/") def index(): return "Login"

Step 3: Create HTML Forms
    - Type 'html' and use a Doctype
    - Change the title to your desire title
    - In the body of the Doctype, create a 'Header'
    - Create a jinja to a body and end block '{% block body%} {% endblock %}'
    - In the index file create a 'header'
    _ Create a form action and use an input action for 'username and 'password' 

Step 4: Create a Login Session
    - in your main.py file 
    - pass an argurnment in the route (if "username" in session:) 
    - they should be redirected to the dashboard (return redirect(url_for('dashboard')))

Step 5: Set up Database
    - create a database db = SQLAlchemy(app)
    - set up a database model (id = db.column(db.integer, primary_key=True, username = db.column()
    password = db.column()))
    - create a database to store a secure version of user passwords (from werkzeug.security import generate_password_hash) 
    - Than import (check_password_hash) to unhash password 
    - from flask_sqlalchemy import SQLAlchemy and create an (app.secret_key "the_key")
    - configure SQL Alchemy with sqlite ("app.config ["SQLALCHEMY_DATABASE_URI"] = "sqlite://yourdatabasename")
    - Configure sql alchemy not to track (app.config["SQLALCHEMY_TRACK_MODIFICATIONS"] = False)

Step 6: User Ability To Login
    - Create a login, logout, register and dashboard routes, give them a method. (@app.route("/login", methods=["POST"]) def login():)
    _
