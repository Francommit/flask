# flask tutorial

Following along here - https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-ii-templates

## Chapter 1

Python 3 version, virtual environment support 
`sudo apt-get install python3-venv
python -m venv venv`

NOTE: any version of Python older than 3.4 (and that includes the 2.7 release), virtual environments are not supported natively.

activate your brand new virtual environment (windows)
`venv\Scripts\activate`

install flask now
`pip install flask`

In Python, a sub-directory that includes a __init__.py file is considered a package, and can be imported. When you import a package, the __init__.py executes and defines what symbols the package exposes to the outside world.

so to run your flask_app you need to usually set environment variables like this
`set FLASK_APP=microblog.py`

then you can run your app handy dandy - http://127.0.0.1:5000/
`flask run`

BUT - We want to automatically run these environment variables
this can be done but using this command
`pip install python-dotenv`

Then you can just write the environment variable name and value in a .flaskenv file in the top-level directory of the project

## Chapter 2