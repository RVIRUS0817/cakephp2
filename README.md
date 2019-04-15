# cakephp2.10

![logo-2](https://user-images.githubusercontent.com/5633085/56077045-8b3d8d80-5e12-11e9-8f04-6ea41ec2ba54.jpg)

tutorials

- cakephp2.10
- php7.2

## dev

- start dev container

```
$ cd 
fork my repository
$ cd docker
$ docker-compose build
$ docker-compose up -d
$ docker exec -it docker_phpfpm_1 sh
$ cd /var/www/html/cakephp2
$ Vendor/bin/cake bake project /var/www/html/cakephp2
$ composer create-project --prefer-dist cakephp/app my_app
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

