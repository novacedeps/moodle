# Setup moodle

## Quickstart

https://docs.digitalocean.com/products/container-registry/getting-started/quickstart/

## Build image & push in docker registry

```bash
docker build . -t registry.digitalocean.com/moodle-registry/moodle:401
docker push registry.digitalocean.com/moodle-registry/moodle:401
```

## Export db with docker

```sh
docker run --rm mysql:8 sh -c 'exec mysqldump -h[HOST_REMOTO] -P[PORT] -u[USER] -p"$MYSQL_PWD" moodle' > backup-remote.sql
```