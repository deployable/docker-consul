# consul compose definition

A docker compose definition for a [consul](https://consul.io)  network, including [registrator](http://gliderlabs.com/registrator/latest/)

3 servers
2 agents
1 registrator

The `basic_config.json` file is mounted into each consul instance. The hashicorp "ping"/update check is disabled.
 
