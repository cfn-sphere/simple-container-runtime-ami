# Instrumentation of scr and docker services

## Context:
SCR requires docker-compose to run a service consisting of one or more docker containers. Docker-compose requires docker to run a service. 
This service might consist of several different but depending docker containers running on an instance. 
To make sure that these containers are started and stopped in the right order docker-compose must be the last service being started and the first one being stopped. 

## Decision:
Docker service autostart is disabled and the scr init config starts/stops docker service according to the scr service state.

## Consequences:
- The service start/stop order is maintained and containers can start/stop as defined in the docker-compose.yml configuration. 
- The deactivated docker service might cause confusion. 
- A manual update of the docker service also might cause problems activating the autostart again (but scr image is designed to be immutable).
