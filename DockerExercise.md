# 🐳 Docker Hands-on Exercise.

I’m sharing Docker exercise for you to practice and strengthen your containerization skills. Please go through the steps carefully and try to complete them on over this long weekends! Happy Dockering! 🚢

Feel free to use the docker official links:
1. https://docs.docker.com/compose/
2. https://docs.docker.com/reference/dockerfile/



### 🧱 Question 1: Build a Custom Nginx Image with Static HTML

**Goal:** <br>
- Use a Dockerfile to serve custom static content with Nginx. Question:
- Create a Dockerfile that uses Nginx and copies a custom index.html file to serve as the homepage.
- Use Docker Compose to build and run the container.

**Requirements:**
- Base image: `nginx:alpine`
- Copy local `index.html` into container. [Download index.html](https://github.com/TechTitans-Academy/experiments-hub/blob/main/Dockerfiles/index.html)
- Expose 80 and map it to port 89 to host
- When visiting `http://localhost:89` the custom page should appear.
- Upload the docker image to your docker-hub and share the name of the image for testing purpose.
---
### 🧱 Question 2: Create a Dockerfile for a Simple Web App
**Goal:** 
Test understanding of image creation.

**Question:**
- Write a Dockerfile that sets up a simple Python Flask app. The app should be copied into the image, necessary dependencies installed, and the app should run on container start.

**Requirements:**
- Base image: `python:3.9-slim`
- Install dependencies from `requirements.txt`
- Expose port `5000`
- Run `app.py` on container start
- Upload the docker image to your docker-hub and share the name of the image for testing purpose.

`app.py`
```
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello():
    return "Hello from Docker!"

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)
```

`requirements.txt`
```
flask
```


---
### <u> 🧱 Question 3: Add a Named Volume for Persistent MySQL databases.</u>
**Goal:** 
- Test understanding of Docker volumes and docker-compose.

**Question:**
- Create a docker-componse.yml file that will create a volume my-sql-data and mount the volume to the /var/lib/mysql folder of Mysql container so that all the table will be persist even after restarting a container.

**Requirements:**
- Base image: mysql
- Mount the volume `my-sql-data` to `/var/lib/mysql`
- Setting up the mysql login password by passing environment variables
	- `MYSQL_ROOT_PASSWORD:root`
	- `MYSQL_DATABASE: testdb`
	- `MYSQL_USER: techtitans`
---
### 🧱 Question 4: Multi-Container docker-compose file.
**Goal:** 
- Get the understanding of docker-compose file with multiple containers.

**Question:**
- Please use the Question-3 docker-compose file for this question and add two ubuntu containers.
- Following are the requirements that you need to add in previous docker-compose.

**Requirements:**
- Base image: ubuntu
- Configure a new network work and attach all the services to it.
- Packages apt update and apt install mysql-client should be installed.
- When docker-compose runs, we should be able to connect the mysql container from ubuntu containers with mysql -h <host> -u root -p command.
**Hit:** Create custom docker image of ubuntu with above packages and then use build option in the docker-compose.yml file.
---
### 🧱 Question 5: 

- How to check the logs of the docker-compose.
- What does "docker-compose up --build" do?
- Which docker-compose command builds the containers without starting them? I want to build the docker-compose only and do not want run the application.




