# AMP Docker

Dockerized version of the good old AMP stack to get you up and running in no time. With PHP 7.1

## What's in the box

- PHP7.1
- Apache Httpd v2.2 (with mod_php)
- MySQL 5.7

## Getting started

1. Clone this repository

        git clone git@github.com:quarkgluant/docker-pamp.git
        
2. Create a symlink named `src` from the PHP project into the `docker-pamp` directory

        ln -s /Path/to/PHP/project docker-pamp/src

3. Copy default configuration files into the PHP docker directory

        cp docker-pamp/defaults/* docker-pamp/php71
        
4. Bring up the AMP7.1 stack. It use the same port 80.

        docker-compose up php71
        
5. Checkout your website at `127.0.0.1`

# Initializing a database

SQL files inside the `mysql` directory will be executed on docker-compose up (with some caveats). This is particularly useful to create an initial database and/or tables.
