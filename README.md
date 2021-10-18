# Guacamole with docker-compose
Apache Guacamole is a clientless remote desktop gateway. It supports standard protocols like VNC, RDP, and SSH.
http://guacamole.apache.org/

## Quickstart
```
git clone https://github.com/edagca/docker-guacamole.git
cd docker-guacamole/
docker-compose up -d
```
Your guacamole server should be available at `http://HOST_IP:8080/guacamole`. The default username is `guacadmin` with password `guacadmin`. This user should be cloned and deleted ASAP.

### To shutdown Guacamole server:
```
docker-compose down
```
### To reset/delete Guacamole data (database)
```
docker volume rm docker-guacamole_mysql_data
```

#### Notes:
The `initdb.sql` file was created as per https://guacamole.apache.org/doc/gug/guacamole-docker.html 
```
docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --mysql > initdb.sql
```
You may recreate your own initdb.sql or use the one in this repository.
