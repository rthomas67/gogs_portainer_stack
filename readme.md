# Summary
This is a docker_compose.yml file to use with Portainer to create a stack
with Gogs and MariaDB on Docker for Raspberry Pi

# Notes
* If GOGS is set up to use Sqllite, it works fine as a single container and this is not needed.

# Setup
* This is meant to create a stack (with it's own network and DNS) so that
the GOGS container can be configured to use MariaDB (MySQL).
* The GOGS config will end up in the host volume mapped to /data in the container in the file: ./gogs/conf/app.ini
  * Edit the "custom" config there (on the host where there is more likely an editor installed)
  and set the db host, pw etc. to match what is set up in the container/stack
* See: https://github.com/gogs/gogs/blob/master/Dockerfile.rpi

# Sample Config DB Section
* See: https://gogs.io/docs/installation
* See: https://gogs.io/docs/installation/configuration_and_run
```
[database]
DB_TYPE  = mysql
HOST     = gogs-mariadb:3306
NAME     = gogs
USER     = root
PASSWD   = gogs_db_999
SSL_MODE = disable
```