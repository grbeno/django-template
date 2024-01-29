## Django sample project
---
- django 4.2.7, custom user model, staticfiles, postgres.
- prepared to deploy: requirements.txt, environs, whitenoise, gunicorn.
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
  - ``` DATABASE_URL=postgres://postgres:<password>@localhost:5432/<database> ```

- Migrate the models to database & run collectstatic for the static files

  - ``` $ pipenv shell ```
  - ``` $ python manage.py migrate ```
  - ``` $ python manage.py collectstatic --noinput ```
    
- Run on localhost
  -  ``` $ python manage.py runserver ```
  
- Initialize your own git repo and commit/push to github
