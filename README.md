# ghost-docker
Dockerized self-hosted Ghost blog made easy

## Deployment
- Change environment in **stack.yml** file
- Init swarm mode via `sudo docker swarm init`
- Create **nginx** network via `sudo docker network create -d overlay --attachable nginx`
- Deploy Ghost 3 via `sudo docker stack deploy -c stack.yml ghost`
- Spin up nginx container with **nginx** network with `proxy_pass http://blog:2368/;`
- You are amazing! :tada:
