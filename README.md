# Simple Web Application

This is a simple web application using [Python Flask](http://flask.pocoo.org/).
  
  Below are the steps required to get this working on a base linux system.
  
  - **Install all required dependencies**
  - **Install and Configure Web Server**
  - **Start Web Server**
   
## 1. Install all required dependencies
  
  Python and its dependencies
  ```bash
  apt-get install -y python3 python3-setuptools python3-dev build-essential python3-pip default-libmysqlclient-dev
  ```
If you are running your code on a macOS you can simply run the following code:
```bash
python3 -m venv env && source env/bin/activate&& pip install flask
```
   
## 2. Install and Configure Web Server

Install Python Flask dependency
```bash
pip3 install flask
```

- Copy `app.py` or download it from a source repository
- Configure database credentials and parameters 

## 3. Start Web Server

Start web server
```bash
FLASK_APP=app.py flask run --host=0.0.0.0
```

## 4. Test

Open a browser and go to URL
```
http://<IP>:5000                            => Welcome
http://<IP>:5000/how%20are%20you            => I am good, how about you?
```

## 5. Docker commands:

```bash
docker build -t myflaskapp:0.1 .
docker run -p 8080:8080 myflaskapp:0.1

docker login

docker tag myflaskapp:0.1 mihirp911/myflaskapp:0.1
docker push mihirp911/myflaskapp:0.1
```