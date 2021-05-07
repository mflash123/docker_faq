# Docker Frequently Asked Questions

* Start magic / start docker - ```docker-compose up```

* Execute command into container - ```docker exec -it <CONTAINER> COMMAND```
ex: ```docker exec -it b90cf7974152 /bin/sh```
  
* List docker containers - ```docker ps```
* List docker containers (include stoped) - ```docker container ls -a```
* Remove docker container - ```docker rm <ID> or <Name> -f```

Config samples : binbot
