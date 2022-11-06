# Desafio buzzvel

## install and run projects

### Prerequisites
* docker installed
* you must have the environment variables of the projects (frontend: buzzvel-front and backend: buzzvel)
properly placed in an .env file (in the frontend the env file name is .env.example ), you will find the default configuration of this
file in the env.example file of each corresponding folder
----

#### steep one
run this command of git for get all modules
~~~~
git clone --recurse-submodules https://github.com/angelomonasterios/challenge-buzzvel.git~~~~
~~~~

#### steep two
create a subnet for a projects
~~~~ 
docker network create  --driver=bridge  --subnet=172.28.0.0/16  --ip-range=172.28.5.0/24  --gateway=172.28.5.254 app_subnet

~~~~
#### steep three
execute this command up containers
~~~~
docker-compose up -d --build
~~~~


#### steep fourth
execute this command to install dependencies
~~~~
docker exec -it buzzvel composer install
~~~~


#### steep five 
execute this command to migrations
~~~~
docker exec -it buzzvel php artisan migrate
~~~~


