# PHP App on Docker

This is my base `docker-compose.yml` definition to start work with a PHP project. It's based on an [article from my blog](https://szymonkrajewski.pl/set-up-muti-container-environment-using-docker-compose/). This repository has the framework-agnostic nginx setup – you have to change the vhost configuration to run e.g. Symfony framework. Additionaly, we mount an external `php.ini` file to the `php-fpm` container.

```sh
docker-compose up -d
```

## What is inside?

* PHP 7.2
  * iconv 
  * mcrypt 
  * mysqli 
  * pdo_mysql 
  * mbstring 
  * intl
* nginx 1.11
* MariaDB 10
  * default database: `app`
  * root password: `root`

### Exposed ports:

* nginx:80 -> 8080
* db:3306 -> 33060
