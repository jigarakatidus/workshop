Create Network:
```docker network create todo```

Create Web
```docker run -d --network todo --name web -p 80:80 -v $(PWD):/var/www/html workshop```

Create DB
```docker run -d --network todo --name db -p 3306:3306 -e MYSQL_ROOT_PASSWORD=secret -v ./data:/var/lib/mysql mysql:8.0```

Login Into DB Container
```docker exec -it db bash```

Truncate DB
```TRUNCATE TABLE todoapp```

Access localhost