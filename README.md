## Django sample project
---
- django 4.2.7, custom user model, staticfiles, whitenoise, gunicorn, postgres.   
---

### How to use

- Download the zip file
- Create your own virtual environment on your project directory and install the required libraries/packages. (pipenv) 
  - ```$ pipenv install -r requirements.txt```

- Create postgres database on your local system

  - ``` # Download & install postgres ```
  - ``` psql -U postgres ```
  - ``` CREATE DATABASE <db_name> WITH OWNER postgres; ```

- Create .env file that includes DEBUG, SECRET_KEY, SSL_REQUIRE, DATABASE_URL values

  - ``` # Generate secret key ```
  - ``` $ python -c 'import secrets;print(secrets.token_urlsafe())' ```

- Migrate the models to database & run collectstatic to static files

  - ``` $ pipenv shell ```
  - ``` $ python manage.py migrate ```
  - ``` $ python manage.py collectstatic --noinput ```
  
- Initialize your own git repo and commit/push to a github repository  
