# Prepare a Docker config

Since Docker and docker-compose already come preinstalled, this step is simple:

`wget https://raw.githubusercontent.com/jbemmel/katacoda-scenarios/main/Testing-Jitsi-at-Scale/docker-compose.yml`{{execute}}

Run docker-compose:

`docker-compose up`{{execute}}

For higher scale testing (more users), use e.g.

`export COMPOSE_PARALLEL_LIMIT=1000;docker network prune --force;docker-compose up -d --scale node=3`{{execute}} => 3 browsers per container (you can go up to ~100)
