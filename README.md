# Simple Web Application -  Dynamically Paramerter Application color through Docker Environment variable (Database configuration is not included)

This is a simple web application using [Python Flask](http://flask.pocoo.org/)
  
  Below are the steps required to get this working on a base linux system.
  
  - Install all required dependencies
  - Install and Configure Web Server
  - Start Web Server
   
## 1. Install all required dependencies
  
  Python and its dependencies

    apt-get install -y python python-setuptools python-dev build-essential python3-pip python3-mysqldb

   
## 2. Install and Configure Web Server

Install Python Flask dependency

    pip install flask
    pip install flask-mysql

- Copy app.py or download it from source repository

## 3. Start Web Server

Start web server

    FLASK_APP=app.py flask run --host=0.0.0.0
        
## 4. Test

Open a browser and go to URL

    http://<IP>:5000                            => Welcome

## 5. Running from Docker 

     docker build . -f Dockerfile -t my-simple-webapp-color
     docker run -e APP_COLOR=blue -d my-simple-webapp-color

    
