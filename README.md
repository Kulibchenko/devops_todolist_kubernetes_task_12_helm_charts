# Writing Helm Charts
    
  This project involves converting a Dockerized To-Do application into a Helm chart for deployment on a Kubernetes cluster running on Kind. The Helm chart consists of two sub-charts: todoapp and mysql, ensuring modular and scalable deployment. Configurations such as namespace, secrets, resource limits, rolling updates, node affinity, and persistent storage are managed via values.yaml. A bootstrap.sh script automates cluster setup, node tainting, and Helm chart deployment. Dependencies are explicitly defined, ensuring the todoapp waits for mysql to be ready. 


## Explore

Try it out by installing the requirements (the following commands work only with Python 3.8 and higher, due to Django 4):

```
pip install -r requirements.txt
```

Create a database schema:

```
python manage.py migrate
```

And then start the server (default is http://localhost:8000):

```
python manage.py runserver
```

Now you can browse the [API](http://localhost:8000/api/) or start on the [landing page](http://localhost:8000/).

## To validate our solution run bootstraps.sh and after cluster spin up open link

    http://localhost:30007/

You must see our web app todoapp
