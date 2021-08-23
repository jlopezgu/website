# docker-compose Django Mysql

**docker-compose Django Mysql** is a Python example that implements basic Django implementation along with a Mysql 
instance running in a docker container. Docker-compose implements volumes that allow persistence of data 
even if the container has been shut down or destroyed.

## Installation
Cloning the code into local.
```shell
git clone https://github.com/jlopezgu/website.git
```

Use the package manager to install dependencies.
```shell
pip install -r requirements.txt
```

## Running locally
Before running Django make sure you have a mysql instance running with correct ports and properly configured in 
**/website/website/settings.py**
```shell
python manage.py runserver 0.0.0.0:8000
python manage.py makemigrations
python manage.py migrate
python manage.py createcachetable
python manage.py createsuperuser --noinput --username admin --email admin@example.com
```

## Running on docker-compose
First you need to install [docker-compose](https://docs.docker.com/get-docker/)
```shell
docker-compose up
```

## License
[MIT](https://choosealicense.com/licenses/mit/)