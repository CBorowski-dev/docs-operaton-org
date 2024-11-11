---

title: "Run Operatonusing Docker"
weight: 20

menu:
  main:
    name: "Docker"
    identifier: "installation-guide-docker"
    parent: "installation-guide"
    pre: "Run the Full Distribution using Docker"

---

# Community Edition

The Community Edition docker images can be found on [GitHub](https://github.com/camunda/docker-camunda-bpm-platform) and [Docker Hub](https://hub.docker.com/r/camunda/camunda-bpm-platform/).

## Start Operaton Run using Docker

To start [Operaton Run]({{< ref "/user-guide/camunda-bpm-run.md" >}}) execute the following commands:

```shell
docker pull camunda/camunda-bpm-platform:run-latest
docker run -d --name operaton -p 8080:8080 camunda/camunda-bpm-platform:run-latest
```

## Start Operaton (Tomcat) using Docker

To start Operaton, execute the following commands:

```shell
docker pull camunda/camunda-bpm-platform:latest
docker run -d --name operaton -p 8080:8080 camunda/camunda-bpm-platform:latest
```

Please note that by default the Apache Tomcat distribution is used. For a guide on how to use one of the other distributions, see the [tag schema](https://github.com/camunda/docker-camunda-bpm-platform#supported-tagsreleases).