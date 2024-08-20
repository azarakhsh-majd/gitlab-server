docker compose up -d

docker ps : export command: 

1- a2b0a0216e8c   gitlab/gitlab-ce:latest            "/assets/wrapper"        7 days ago    Up About a minute (healthy)   22/tcp, 80/tcp, 443/tcp, 0.0.0.0:8088->8088/tcp, :::8088->8088/tcp  gitlab-server

2- 0fb9c9fb28c3   gitlab/gitlab-runner:alpine        "/usr/bin/dumb-init …"   7 days ago    Up About a minute 

create new project --> setting --> CICD --> runner --> new project runner --> create runner --> type runner --> 

step 1: gitlab-runner register  --url http://172.25.117.106:8088  --token glrt-2t_b8swAKAhj3QyFKD9h --> set this coommand in container gitlab-runner:

docker exec -it gitlab-runner  /bin/bash

 gitlab-runner register
 
 Enter the GitLab instance URL : http://gitlab-reg.local:8088/
 
 --token glrt-2t_b8swAKAhj3QyFKD9h

 Enter a name for the runner. This is stored only in the local config.toml file: runner-1
 
 Enter an executor: shell, parallels, kubernetes, docker, docker-windows, docker+machine, docker-autoscaler, instance, custom, ssh, virtualbox: docker
 
 Enter the default Docker image (for example, ruby:2.7): alpine
 
 export command: Configuration (with the authentication token) was saved in "/etc/gitlab-runner/config.toml"
