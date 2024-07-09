Tracks
======

A Docker build resources for Get On Tracks GTD app.

Forked form https://github.com/eyecreate/tracks

Remember to have Docker Desktop running prior to running any of the Docker commands below.

## Versions

The `versions` directory contains docker files to build specific versions of tracks.

These download the zip files from the tracks archive during the build process.

Readme files are contained in the folders.

These have been released as tagged versions to docker hub.


### Tracks v 2.3.0

```
docker run -p 80:80 eviltester/tracks:2.3.0
```

### Tracks v 2.2.3

```
docker run -p 80:80 eviltester/tracks:2.2.3
```


## To Use via Docker from Docker Hub

```
docker run -p 80:80 eviltester/tracks
```

https://hub.docker.com/r/eviltester/tracks/tags

For version 2.3.0 of tracks

```
docker run -p 80:80 eviltester/tracks:2.3.0
```

Tracks will then be running on port 80

```
http://localhost:80
```


## To Use via Docker Locally

Build the image locally, then run it:

```
docker build --tag 'tracks' .
```

Then run it:

```
docker run -p 80:80 "tracks"
```

or

```
docker run -d --name=tracks -p 80:80 "tracks"
```

Then visit:

http://localhost:80

If you find that you can't login or can't create an admin session then try opening the link in incognito mode... if that works then delete the "_tracksapp_session" cookie in your normal browser window.


## To use via Docker Compose Locally

Docker compose is using the official release images for mariadb and tracks.

```
docker compose up
```

Create the database

```
docker exec -it tracksdocker-web-1 sh
```

Then in the shell

```
bundle exec rake db:reset
```

Then visit:

```
http://localhost:3000
```




Tracks
======

Tracks is a web-based application modelling Allen's Getting Things Done methodology.

https://www.getontracks.org/


This repo was forked and based on https://github.com/eyecreate/tracks

 



