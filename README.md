# rails-mysql-docker-compose
setup docker-compose including Rails & MySQL 

## environment

```shell script
ruby: 2.7.0
rails: 6.0.2.1
mysql: 5.7.12
```

## getting started rails new

```shell script
# rename current directory to Rails App name
$ cd ..
$ mv rails-chromedriver-docker-compose/ <APP_NAME> 

# Create Rails project in the current directory
$ docker-compose run app rails new . --database=postgresql

# edit database.yml
- host: localhost
+ host: <%= ENV['APP_DATABASE_HOST'] %>

# build
$ docker-compose up --build

```
