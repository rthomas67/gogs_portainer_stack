# Summary
This is a docker_compose.yml file to use with Portainer to create a stack
with Gogs and MariaDB on Docker for Raspberry Pi

# Setup
If GOGS is set up to use Sqllite, it works fine as a single container.
This is meant to create a stack (with it's own network and DNS) so that
the GOGS container can be configured to use MariaDB (MySQL)

