# consul compose definition

A docker compose definition for a [consul](https://consul.io)  network, including [registrator](http://gliderlabs.com/registrator/latest/)

Includes definitions for running 3 servers, 2 agents and 1 registrator in a cluster on a single Docker node.

Based on the default [`consul`](https://hub.docker.com/_/consul/) image. 

The `basic_config.json` file is mounted into each consul instance. The hashicorp "ping"/update check is disabled.
