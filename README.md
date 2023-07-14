# docker-mysql-shell-batch

Docker HUB: https://hub.docker.com/r/waveoffire/mysql-shell-batch

Image for executing sql scripts from .sql files, using mysqlsh - mysql shell tool



Usage:
```
docker run --name test -v /path/to/scripts/:/scripts/ -e MYSQL_USER=username -e MYSQL_HOST=ip_or_hostname_of_mysqlinstanc
e -e MYSQL_PORT=3306 -e MYSQL_PASSWORD=password -e MYSQL_SCRIPT=/scripts/cluster.sql waveoffire/mysql-shell-batch
```
Usage in docker-compose:


    mysql-shell:
        image: waveoffire/mysql-shell-batch
        container_name: mysql-shell-batch-1
        volumes:
            - ./scripts/:/scripts/
        environment:
            - MYSQL_USER=username
            - MYSQL_HOST=ip_or_hostname_of_mysqlinstance
            - MYSQL_PORT=3306
            - MYSQL_PASSWORD=password
            - MYSQL_SCRIPT=/scripts/cluster.sql
