# consul compose definition

A docker compose definition for a [consul](https://consul.io)  network, including [registrator](http://gliderlabs.com/registrator/latest/)

Base on the default [`consul`](https://hub.docker.com/_/consul/) image and includes definitiosn for 3 servers, 2 agents and 1 registrator

The `basic_config.json` file is mounted into each consul instance. The hashicorp "ping"/update check is disabled.
 
