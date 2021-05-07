# Docker Frequently Asked Questions

* Start magic / start docker - ```docker-compose up```

* Execute command into container - ```docker exec -it <CONTAINER> COMMAND```
ex: ```docker exec -it b90cf7974152 /bin/sh```
  
* List docker containers - ```docker ps```
* List docker containers (include stoped) - ```docker container ls -a```
* Remove docker container - ```docker rm <ID> or <Name> -f```

Config samples : binbot

# Docker comments
Докер - это по сути ВМ, внутри докера можно создавать контайнер к каждому сервису. Например, контайнер на бек, фронт, базу и тд.

Суть докера, что он создает среду в которой вертится мой код.
Мой код монтируется напрямую в контейнер, и изменяя код на хостевой машине, он автоматически меняется на гостевой. Потому что гостевая смонтирована на дирректирию моего хоста. (Может можно и создавать копию, но в моих конфигах в binbot это так.)

Важные файлы
docker-compos.yml - там я собираю среду, указываю контейнеры.
Говорю какой пхп взять, какой сервер и пр.

Dockerfile -  это постустановочный сценарий, например там я кручу верчу composer, собираю проект.
Там же мне надо придумать схему с .env
