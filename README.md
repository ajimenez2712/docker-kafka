Kafka in Docker
===

This repository provides everything you need to run Kafka in Docker.

Why?
---
The main hurdle of running Kafka in Docker is that it depends on Zookeeper.
Compared to other Kafka docker images, this one runs both Zookeeper and Kafka
in the same container. This means:

* No dependency on an external Zookeeper host, or linking to another container
* Zookeeper and Kafka are configured to work together out of the box

Run
---

```bash
docker run --rm -p 2181:2181 -p 9092:9092 \
  --env ADVERTISED_HOST=localhost \
  --env ADVERTISED_PORT=9092 \
  docker-kafka
```

In the box
---
* **ajimenez2712/kafka**

  The docker image with both Kafka and Zookeeper.

Public Builds
---

https://registry.hub.docker.com/u/ajimenez2712/kafka/

Build from Source
---

    docker build -t ajimenez2712/kafka .

Todo
---

* Not particularily optimzed for startup time.
* Better docs
