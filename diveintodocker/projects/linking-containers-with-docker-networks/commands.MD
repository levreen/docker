## Build docker image
```
docker image build -t web2 .
```
*web2 you change it to your docker_image.

## Check docker network list
```
docker network ls
```
## Inspect docker network
```
docker network inspect
```
***you can add the specific network you want to inspect**
## Run redis 
```
docker container run --rm -itd -p 6379:6379 --name redis redis:3.2-alpine
```

## Stop running docker container
```
docker stop >docker-container-name<
```

## Inspect docker container network using redis/container-web-name
```
docker exec redis ifconfig
``` 
###### OR
```
docker exec web2 ifconfig
```
***web2 change it to your docker image***
###### *Note: at the Dockerfile add on the RUN command 
```
RUN apk update & apk add iputils
```
## Using exec
```
docker exec redis cat /etc/hosts
```

## Redis cli
```
docker exec -it redis redis-cli
```

## Run Docker Volume
```
docker volume create >name-of-your-container<
```

## Run redis with volume
```
docker container run --rm -itd -p 6379:6379 --name redis --net firstnetwork -v web2_redis:/data redis:3.2-alpine                                   
```

## Redis commond to have persistence memory
```
docker exec redis redis-cli SAVE
```
***know where the data resides***