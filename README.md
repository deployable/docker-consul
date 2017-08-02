# Consul Cluster - Docker Compose Definition

A docker compose definition for a [consul](https://consul.io) network, including [registrator](http://gliderlabs.com/registrator/latest/) based on the default [`consul`](https://hub.docker.com/_/consul/) image.

The definition includes 3 servers, 2 agents and 1 registrator in a cluster on a single Docker node.

To start the cluster

    docker-compose up -d

To inspect the logs

    docker-compose logs

To init data

    docker-compose -f docker-compose-init.yml run consul_init

To reset

    docker-compose down -v

The `basic_config.json` file is mounted into each consul instance. The hashicorp "ping"/update check is disabled.
