# flask tutorial

Following along here - https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-ii-templates

## Chapter 1

Install python 3 in Windows:  
`choco install python3 -y`  

Initialize your virtual env directory:  
`python -m venv venv`  

NOTE: any version of Python older than 3.4 (and that includes the 2.7 release), virtual environments are not supported natively.  

Activate your brand new virtual environment (windows)  
`venv\Scripts\activate`  

**BOOM** you're working with a virtual python directory.
Let's setup what we need for flask.  

Install flask:  
`pip install flask`  
` python -m pip install --upgrade pip`

In Python, a sub-directory that includes a __init__.py file is considered a package, and can be imported. When you import a package, the __init__.py executes and defines what symbols the package exposes to the outside world.  

So to run your flask_app you need to usually set environment variables like this:  
`set FLASK_APP=microblog.py`  

Then you can run your app handy dandy - http://127.0.0.1:5000/  
`flask run`  

**BUT** We want to automatically use these environment variables.  
This can be done but using this library:  
`pip install python-dotenv`  

Then you can just write the environment variable name and value in a .flaskenv file in the top-level directory of the project

## Chapter 2

Templates help achieve this separation between presentation and business logic. In Flask, templates are written as separate files, stored in a templates folder that is inside the application package.

The render_template() function invokes the Jinja2 template engine that comes bundled with the Flask framework. Jinja2 substitutes {{ ... }} blocks with the corresponding values, given by the arguments provided in the render_template() call.

Templates also support control statements, given inside {% ... %}

Jinja2 has a template inheritance feature that specifically addresses this problem. In essence, what you can do is move the parts of the page layout that are common to all templates to a base template, from which all other templates are derived.

Define a base template called base.html that includes a simple navigation bar and also the title logic I implemented earlier.

