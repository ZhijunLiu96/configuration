# Deploy app to hero

Example: python plotly app, Python 3


## Create a Virtual Envirenment in Terminal
1. install virtualenv
```
$ pip install virtualenv
```
2. Create your virtual environment "venv", (you can change to any name you like)
```
$ cd /SetPath
$ python -m virtualenv venv
```
3. Activate the virtual environment (**MAC OS**)
```
$ source venv/bin/activate
```

## Install Python Packages
1. You can install python packages one by one (using ```pip install```).
2. Or generate a requirements.txt file both manually or 
```
$ pip freeze > requirements.txt
```
```
$ pip install -r requirements.txt
```
or wirte a list of packages you want to install, inside the requirements.txt file </br>
```
catalogue==1.0.0
certifi==2020.6.20
chardet==3.0.4
click==7.1.2
cycler==0.10.0
cymem==2.0.3
dash==1.13.4
```
then </br>
```
$ pip install -r requirements.txt
```

## Generate Some Other Files 
1. ```.gitignore``` file. You can create a txt file and then rename it to ```.gitignore```. You can write the names of files that you don't wnat to upload.
```
venv
*.pyc
.DS_Store
.env
```
2. Generate a ```Procfile``` file, with the following content, used for deployment.
```
web: gunicorn app:server
```

## Upload Your Work to Remote Repository
1.  Make sure the app.py is bug-free, test it before uploading to remote repository

```
$ python app.py
```

2. Login to heroku

```
$ heroku login
```

3. Use git to do every thing you want ~

```
$ git init
$ heroku create <repo>
```

```
$ git clone
```

```
$ git staus
$ git add .
$ git commit -m "comment"
$ git push
```

## Open the App
```
$ heroku open
```

## Deactivate Virtual Environment
```
$ deactivate
```

