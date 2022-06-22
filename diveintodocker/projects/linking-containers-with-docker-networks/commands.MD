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
## OR
```
docker exec web2 ifconfig
```
*web2 change it to your docker image
### *Note: at the Dockerfile add on the RUN command 
```
RUN apk update & apk add iputils
```

