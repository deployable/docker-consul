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

### Port Mappings

Server 1
 - '8310:8300/udp'
 - '8311:8301/udp'
 - '8312:8302/udp'
 - '8411:8400/tcp'

Server 2
 - '8320:8300/udp'
 - '8321:8301/udp'
 - '8322:8302/udp'
 - '8412:8400/tcp'

Server 3
 - '8330:8300/udp'
 - '8331:8301/udp'
 - '8332:8302/udp'
 - '8413:8400/tcp'

Client 1
 - '8421:8400/tcp'
 - '8521:8500/tcp'
 - '8621:8600/udp'
 - '8621:8600/tcp'

Client 2
 - '8422:8400/tcp'
 - '8522:8500/tcp'
 - '8622:8600/udp'
 - '8622:8600/tcp'

The `basic_config.json` file is mounted into each consul instance. The hashicorp "ping"/update check is disabled.
