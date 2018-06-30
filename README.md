# Docker Lamp

A simple Docker setup to run PHP, Nginx and MariaDB. It was made for my personal use. But if it will be useful to you, feel free use and contribute!

## Instructions

You need to have [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/) installed on your machine.

*In some case, you'll have to use **sudo** to run some commands presented here. It will depend on how you installed the applications on your system.*

* Clone the repository
* Change the configs (if necessary)
* Run ```docker-compose up```

## Images

* **Nginx**: nginx:latest
* **PHP**: php:7-fpm
* **MariaDB**: mariadb:latest

## With everything working...

### Nginx

The server will be running on port **8080** and serving files from the **code** directory. If you want or need another **server name**, just change the *server_name* variable in the *site.conf* file (remember to add an entry on your host file pointing to 127.0.0.1).

Point your browser to **http://localhost:8080** and be happy!

### PHP

PHP will also serve files from the **code** directory. By default, I left an *index.php* file echoing a *phpinfo()* function. The **log** config is in the *log.conf* file.

### MariaDB

The database will be running on port **3306** and the default root password is *123456*. All the data will be stored in the **data** directory.

To access the database from the terminal, run the command:

```mysql -uroot -p123456 -h localhost -P 3306 --protocol=tcp```

## I know...

Yeah, I know that some improvments are necessary. But, it is working for me at the moment. As soon as I make them, I will update this setup project.

Again, feel free to contribute!

Thanks!

💙 🤟
