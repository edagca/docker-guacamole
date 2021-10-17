# Guacamole with docker-compose

# Quickstart
```
docker-compose up -d
```

The initdb.sql file was created by:
```
docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --mysql > initdb.sql
```
