# Guacamole with docker-compose

## Quickstart
```
git clone https://github.com/edagca/docker-guacamole.git
cd docker-guacamole/
docker-compose up -d
```
Your guacamole server should now be available at `http://HOST_IP:8080/guacamole`. The default username is `guacadmin` with password `guacadmin`. This user should be cloned and deleted ASAP

#### Notes:
The `initdb.sql` file was created as per https://guacamole.apache.org/doc/gug/guacamole-docker.html 
```
docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --mysql > initdb.sql
```
You may recreate your own initdb.sql or use the one in this repository.
