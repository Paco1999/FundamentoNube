# Parcial 1 - Francisco Jose Zamudio Aguilar

## DCF (Docker compose file)

It is the one that will define the version, services, network, volumes, configurations and secrets of the container. This repository will only use the first two.

## DCV (Docker compose version)

The version of the composition format will be set.

The most advisable thing is to use the latest version, because it can happen that the files in the window require a specific version, and this is due to the version of the engine that the window has.

## DCS (Docker compose services)

Now we will go to the computer resources that the container has, this is where we are going to define the services to be used.

In the repository you will find:

IMAGE- It is the one that will define the image of the window that will manage the container.

RESTART- It is the one that will define the policy of the platform when the container is stopped.

ALWAYS- If the container is stopped, it will help us to restart by default.

In the event that it is stopped manually, the daemon has to react or in that case, restart it manually.

ENVIRONMENT- It is the one that defines the values ​​of the environment variables.

PORTS- It is the one that defines in which port the container will be executed.

VOLUMES- It is the one that will define the host folders that are inside the window container, it will also help to synchronize the container with the folders.

## Folders

In the repository there will be the following folders that will be the containers:

- db
- web

## Db

In the DB folder we will find a docker container that will open a database made with MariaDB.

Next, the subfolders of the container will be mentioned:

CONF- Here the database configuration will be defined.

FILES- Here are the main files of the database.

LOGS- Here are the database records.


Customized services:

IMAGE- The latest version of MariaDB's Docker container.

RESTART- Always.

PORTS-3306, is the port where it will be executed.

VOLUMES- The folders that are synchronized with the container are created here. 

The composition file of the window that is inside this same folder, we can find:

MYSQL_ROOT_PASSWORD- The root password is defined.

MYSQL_DATABASE- Here you will define the name that the database will have when the image is executed.

If you define a username and password below it, you will have full access to it.

MYSQL_USER with MYSQL_PASSWORD- The database user is defined.

MYSQL_PASSWORD with MYSQL_USER- The password is defined.

## Web

In the WEB folder there is a window container for a web application, which was created with PHP and HTML.

Also here we will find the docker-compose yml file and the APP source code folder.

Customized services:

IMAGE- Latest version, in this case 7.4, of the image of the webdevops / php-nginx window: 7.4.

RESTART- Always.

PORTS- It will be executed on port 80.

VOLUMES- Here it is defined that the application folder has the source code.

We can also find:

MEASUREMENTAPP- Here we will define the name of the container, and what is inside it will be part of the configuration.

The configuration of this is:

PHP_DISPLAY_ERRORS- Returns the errors that are within the application. 
