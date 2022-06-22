# Updates:
#   Nov 2019: Update Flask to a more recent version
Flask==2.1.0


## Docker Commands/Flags

### Running docker container after docker build
```docker
docker container run -it -p 5000:5000 -e FLASK_APP=app.py --rm --name web1 -e FLASK_DEBUG=1 -v C:\Users\arden\docker\diveintodocker\projects\creating-docker-file:/app web1
```