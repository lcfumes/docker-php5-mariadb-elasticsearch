## lcfumes/docker-php5-machine ##

### Containers ###
Proxy

Centos:7
Nginx
PHP5.6
Php-Fpm
MariaDb:10.0
ElasticSearch: 2.2


This project was made to use with composer.json. To run it alone, you need do change some configurations in the file docker-compose.yml. 

If you wanna run it alone, you can write me. It will be a pleasure to help you.

### Dependencies ###
```
apt-get install curl php5-cli php5-curl
```


### Using in composer.json ###

```
{
    "repositories": [
         {
             "url": "git@github.com:lcfumes/docker-php5-mariadb-elasticsearch.git",
             "type": "git"
         }
    ],

    "require-dev": {
        "lcfumes/docker-php56-mariadb-elasticsearch": "dev-master"
    }
}
```

### Runing Composer ###

Local Machine:

```
composer install
```

Live Machine

```
composer install --no-dev
```

### About the project ###

You need to create a "tmp/nginx" folder, with write permission.

```
cd /project/
mkdir tmp/
mkdir tmp/nginx
chmod -R 777 tmp
```

This project was made to run in the ZendFramework. If you use another framework, my sugestion is to create a simbolic link called "public". 

### Install Docker ###

```
wget -qO- https://get.docker.com/ | sh
```

### Added your user to Docker group ###

```
sudo usermod -aG docker YOUR_USER
```

###  Install Docker-Compose ###

```
https://docs.docker.com/compose/install/
```

## To Run ##

### Up machines ###

```
cd /yourproject/vendor/lcfumes/docker-php56-mariadb-elasticsearch/
docker-compose up -d
```

### Stop ###

```
docker-compose stop
docker-compose rm
```

### Database ###

```
mysql -uroot -proot -hdatabase.dev
```

### Browser ###

```
http://webproject.dev
```

### Docker HUB ###

This project use the images from Docker Hub

lcfumes/nginx-php56 - https://hub.docker.com/r/lcfumes/docker-centos7-php56-mariadb/

jwilder/nginx-proxy - https://hub.docker.com/r/jwilder/nginx-proxy/

Mariadb - https://hub.docker.com/_/mariadb/

ElasticSearch - http://elastic.co
