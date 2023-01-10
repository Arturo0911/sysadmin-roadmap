# Commands to get information from a linux system





## Docker containers


How to copy information from a directory inside a container to host machine


```bash
docker cp <containerId>:/file/path/within/container /host/path/target
```



Running this script you will have a backup from a mysql container

```bash
docker exec CONTAINER /usr/bin/mysqldump -u root --password=root DATABASE > backup.sql
```


Restore the database

```bash
cat backup.sql | docker exec -i CONTAINER /usr/bin/mysql -u root --password=root DATABASE
```


