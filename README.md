# WordPress Docker Container with MariaDB

Complete docker container with Nginx 1.10 & PHP-FPM 7.1 & MariaDB based on Alpine Linux.

_WordPress version currently installed:_ **4.7.4**

## Create

	docker build docker-wordpress-mysql -t wordpress

## Usage
    docker run -d --name wordpress -p 80:80 -v /local/folder:/var/www/wp-content --rm wordpress
    
Or without a volume
    
    docker run -d -p 80:80 --name wordpress --restart always wordpress
    
## Database password
The database password for root and wordpress user are randmly generated on each container generation. For checking it
    docker logs <container>

And find this lines

    GENERATED ROOT PASSWORD AS 'x7tiZcRi7DhZGc3B2mDy4Qb9rOheQX8Qfubd9ZZr'
    
    GENERATED WORDPRESS USER PASSWORD AS 'amOICpa05KYHzaipnaXANxAeg0XgWqHrO4d9ARWD'

### Forked from
* https://github.com/TrafeX/docker-wordpress
