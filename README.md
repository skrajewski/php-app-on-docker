# PHP App on Docker

This is my base `docker-compose.yml` definition to start work with a PHP project. 

```sh
docker-compose up -d
```



## What is inside?

* PHP 7.1
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
* mariadb:3306 -> 33060