### Build docker image
```
docker image build -t web1 .
```
*web1 you can change it to your docker image.

### Running docker container after docker build
```
docker container run -it -p 5000:5000 -e FLASK_APP=app.py --rm --name web1 -e FLASK_DEBUG=1 -v C:\Users\arden\docker\diveintodocker\projects\creating-docker-file:/app web1
```

### Debug docker container
```
docker container exec -it web1 sh
```

### Running Python in docker container
```
 docker container run -it --rm --name testingpython python:3.7.5-alpine python
```
REPL



