# Visualizing Metrics with Grafana

## Setup
For this exercise, we'll use Docker containers, and Docker Compose.  Make sure
you have Docker and Docker Compose installed.  If you're using a Mac, install
[Docker For Mac](https://docs.docker.com/docker-for-mac/install/).

## Running Docker Containers
```sh
docker-compose build
docker-compose up -d
```
Point your browser at http://127.0.0.1:3000, where the Grafana Docker container
is listening.  Log in using the configured Grafana credentials (see the
`GF_SECURITY_ADMIN_USER`, `GF_SECURITY_ADMIN_PASSWORD` environment variables in
`docker-compose.yml`).  Explore around.

To log into the `ubuntu` container, do things to consume CPU, disk, use:
```sh
docker-compose exec ubuntu bash
```

When done, destroy all of the running containers using:
```sh
docker-compose down
```
