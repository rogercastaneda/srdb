## Instructions
This project helps to start the database container and give instructions to use the php7-wpsr image. 

1. Start Database container
```
docker-compose up
```

2. Run the php container
```
docker run -it --rm --name srdb --link="sr_db" --network="srdb_srdb-network" rogercastaneda/php-wpsr:0.1 sh
```

3. Enter to the server container 
```
docker exec -it srdb sh
```

4. Execute Search Replace database command:
```bash
php ./srdb.cli.php -h="sr_db" -n="sr_db" -u="root" -p="root" -s="http://www.site.com" -r="https://www.site.com"
```