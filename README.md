before starting:-
Tools to install
       (1) Must install python latest version
       (2) a ready IDE(integrated development environment) (in my laptop its Visual Studio Code); you can use pycharm or sublime also. 

****************                                    let's get started                                    ********************

at first make a Directory on your IDE

then open a command promt(CMD) and install flask using this command  :- " pip install flask "
if it get's installed then you can check using this command  :- " flask --version "

****************               Introduction                 *****************
inside your directory make your new python file  " market.py "

To go through the full documentation of flask go through this website :-  " https://flask.palletsprojects.com/en/1.1.x/quickstart/ "

at first we will build a minimal application i.e. hello world using flask.

we will learn from very basics:-

at first copy the below code : -

  >>>>                  from flask import Flask
  >>>>                      app = Flask(__name__)
  >>>>
  >>>>                      @app.route('/')
  >>>>                      def hello_world():
  >>>>                          return 'Hello, World!'
    
    
and paste it of the file named " market . py "

now in this code-------
at first we have imported a module named Flask from a package called flask

" __name__ " magic variable ( built in variable which refers to th local python file we are working with )

" @app.route('/') " it is basically a decorator i.e. the root Url 

in order to run our app successifully we are required to setup several environment variable i.e.
 go to your command promt and type these specific words:-
 "
    set FLASK_APP=market.py
 "
 "
    flask run
 "
 
#### something like this would show up:--
             Use a production WSGI server instead.
                   * Debug mode: on
                   * Restarting with stat
                   * Debugger is active!
                   * Debugger PIN: 232-516-006
                   * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
here the application will run on " 127.0.0.1:5000 " this URL
here the ip 127.0.0.1 is a conventional IP address whish is refering to the local machine(localhost)\
and the " 5000 " shown after the colon is the port( the default port for flask application will be 5000 )

after this you must copy the URL and paste it to your browser to see the message " Hello, World! " 

** Note:- this is your first deployed application



***********************       Styling and templating     ************************


now to manipulate the text or to use design :- 
 I Took the help of this website :- http://www.jimshapedcoding.com/courses/Flask%20Full%20Series
 It is a good website which will help you organise the web page and the designing also.
 It is described with step by step implementation on how we will design our web application (mostly the User Interactive Part)
 
 
 *********************        Sending Data to Templates      **********************
 ->   the use of Jinja templating 
          -> Use of jnja for loop to print data from a table
          -> general jina loop syntax  {
          {% for  in  %}
          
          {% endfor %}
          }
          
          -> to use jinja to get dynamic values the syntax is:-
              {{ item.value }} where value is a random variable
 
***********************            authentication using SQL ALCHEMY           **************************

created a database in which username and password will get saved and authentication will be done on the basis
of hashing process so that there may not be or it will be dificult to for a hacker to hack into the database for
the data.

if we want to inport database :these following commanda are required:-

open the command promt and write:- " pip install flask-sqlalchemy "

*** note:- SQLAlchemy is a medium through which we can connect the source code of python with the database.

## for immporting database write python in CMD(to open python interpreter)

(if you want to view your database you can install/use SQLite Viewer)

>>> from (your python file) import db
>>> db.create_all()

this will create a database structure


if you want to add some data into your database you can use add and commit statement like this:-

>>> db.session.add(your database object)
>>> db.session.commit()

if you really want to get all the idea of how to use database manipulation you can see this video:-
(as a reference)
https://www.youtube.com/watch?v=oA8brF3w5XQ&t=2719s


it is a good reference which will describe using flask from basics up to advanced level
i have used this reference to make my project.

