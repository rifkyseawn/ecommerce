# Auction Website

![Image](https://github.com/user-attachments/assets/b7e58149-0517-4810-89e0-30b66001b8f3)

![Image](https://github.com/user-attachments/assets/b0e02097-7d0b-4009-bdd5-3d757b202d2a)

![Image](https://github.com/user-attachments/assets/3891c82e-effb-4cf8-a506-70c5a079fb18)

![Image](https://github.com/user-attachments/assets/d9ed373e-b344-4204-b13d-4cdc503a459f)

![Image](https://github.com/user-attachments/assets/b7a66da7-348a-497d-b200-271c35bbc05b)


An eBay-style e-commerce website developed with **Django 4**, utilizing **HTML5**, **CSS3**, **Bootstrap 5** (Bootswatch theme), and **Chart.js 2** for data visualization. Powered by **PostgreSQL** database.


---


## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Run the Application](#run-the-application)
- [Run the Tests](#run-the-tests)
- [Add Data to the Application](#add-data-to-the-application)
- [Copyright and License](#copyright-and-license)


---


## Prerequisites


Install these essential components:


1. [Python 3.8-3.11](https://www.python.org/downloads/)  
   Required for Django 4.2.4. [Compatibility details](https://django.readthedocs.io/en/stable/faq/install.html)
2. [PostgreSQL](https://www.postgresql.org/download/)
3. [Visual Studio Code](https://code.visualstudio.com/download)


---


## Installation


### 1. Create Virtual Environment


Execute in project root:


```bash
python -m venv venv
```


### 2. Activate Virtual Environment


Execute in project root:


macOS:


```bash
source venv/bin/activate
```


Windows:


```bash
venv\scripts\activate
```


### 3. Install Dependencies


Execute in project root:


```bash
pip install -r requirements.txt
```


### 4. Configure PostgreSQL Database


Remove existing database:


```bash
dropdb --if-exists auctions
```


Access PostgreSQL terminal:


```bash
psql postgres
```


Create database:


```sql
CREATE DATABASE auctions;
```


Create admin user:


```sql
CREATE USER yourusername WITH SUPERUSER PASSWORD 'yourpassword';
```


Exit terminal:


```bash
\q
```


### 5. Setup Environment Variables


Create configuration file:


```bash
touch .env
```


Add configurations:


```bash
SECRET_KEY=yoursecretkey
DEBUG=True
DATABASE_NAME=auctions
DATABASE_USER=yourusername
DATABASE_PASS=yourpassword
DATABASE_HOST=localhost
```


### 6. Apply Database Migrations


Execute sequentially:


```bash
python manage.py makemigrations
python manage.py migrate
```


### 7. Create Admin Account


Run in terminal:


```bash
python manage.py createsuperuser
```


Provide username, email, and password when prompted


## Run the application


```bash
python manage.py runserver
```
Access: http://127.0.0.1:8000


## Run the tests


```bash
python manage.py test --pattern="tests.py"


```


## Add Data to the Application


Add data through Django Admin.


Go to http://127.0.0.1:8000/admin to access the Django Admin interface and sign in using the admin credentials.






