# maven-jdk8-docker

A docker-compose file based on maven-jdk8 that includes docker and docker-compose tools.

To allow the docker tools to work, you need to map in the docker volume:

```
docker run -v /var/run/docker.sock:/tmp/docker.sock maven-jdk8-docker
```

The idea is to use this with the Palantir Junit-Docker-Compose within a GitLab CI environment
(details to come).
