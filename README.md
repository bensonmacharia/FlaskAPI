## Python Flask API
This repository contains source code for a simple python Flask API to illustrate implementation of secure `Authentication` and `Authorization`. After the user is authenticated, a `JWT` access token is generated which is subsequently used to access other protected resources.

## Secure Secrets
Developers often grapple on how to securely use their secrets required by the application such as database credentials. This project also illustrates how such can be saved in a `.env` file which is then referenced within the source code to fetch the secrets. The python `dotenv` library has the method `load_dotenv` to load secrets from the .env file.

## Deployment
```sh
$ git clone https://github.com/bensonmacharia/SecureSecrets
$ cd SecureSecrets
$ pip3 install -r requirements.txt
$ python3 app.py
```
> - The application opens on `http://127.0.0.1:5000/` refer to the accompanied postman collection on how to access the API endpoints
> - Remember to edit the `.env` file to reflect your database settings.

## Use .gitignore
Create a `.gitignore` file and add the path to your `.env` file to prevent it from being committed and uploaded into github while pushing your code.
```sh
$ echo ".env" > .gitignore
$ git add .gitignore
$ git commit -m "add .gitignore file to project"
$ git push origin main
```
If you already committed the .env file to your Git repository, then:-
```sh
$ git rm -r --cached .
$ git add .
$ git commit -m ".gitignore is now working"
```

> Make sure to commit all your important changes before running this, otherwise, you will lose any changes to other files.