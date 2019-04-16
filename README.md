# cakephp2.10

![logo-2](https://user-images.githubusercontent.com/5633085/56077045-8b3d8d80-5e12-11e9-8f04-6ea41ec2ba54.jpg)

tutorials

- cakephp2.10
- php7.2

## dev

First, please refer to 1 if you are starting for the first time.  
Please refer to 2 if you use it after the second time.


- ① If you are starting for the first time

```
fork my repository
$ rm -rf cakephp2.10/cakephp2/cakephp/*
$ cd cakephp2.10/cakephp2/
$ vim cake2.10/cakephp2/cakephp/composer.json

{
    "name": "my_app",
    "require": {
        "cakephp/cakephp": "2.10.*"
    },
    "config": {
        "vendor-dir": "Vendor/"
    }
}

$ cd docker
$ docker-compose build
$ docker-compose up -d
$ docker exec -it docker_phpfpm_1 sh
# cd /var/www/html/cakephp2
# php composer.phar install
# Vendor/bin/cake bake project /var/www/html/cakephp2
# composer create-project --prefer-dist cakephp/app cakephp
```


- ② One that starts from the second time
```
fork my repository
$ cd docker
$ docker-compose up -d
$ docker exec -it docker_phpfpm_1 sh
# cd /var/www/html/cakephp2
# Vendor/bin/cake bake project /var/www/html/cakephp2
```

- change database

```
$ cd cakephp2.10/cakephp2/cakephp/Config
$ cp database.php.default database.php
$ vim database.php
host:mysql
database:my_app
login:root
pass:test
```

- accessl url

http://localhost:8080/

![スクリーンショット 2019-04-15 18 53 33](https://user-images.githubusercontent.com/5633085/56124577-ec4f9780-5fb1-11e9-91ac-f2ad050619a9.png)

