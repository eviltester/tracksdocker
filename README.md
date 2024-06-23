Tracks
======

A Docker build resources for Get On Tracks GTD app.

Forked form https://github.com/eyecreate/tracks

## To Use via Docker

Build the image locally, then run it:

```
docker build --tag 'testtracks' .
```

Then run it:

```
docker run -p 80:80 "testtracks"
```

or

```
docker run -d --name=tracks -p 80:80 "testtracks"
```

Then visit:

http://localhost:80

If you find that you can't login or can't create an admin session then try opening the link in incognito mode... if that works then delete the "_tracksapp_session" cookie in your normal browser window.


## To use via Docker Compose

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

Tracks is a web-based application to help you implement David Allens Getting Things Done™ methodology. It was built using Ruby on Rails.

This is the easy way getting up and running with Tracks, which is one of the greatest software implementations of the GTD™ methodology.

This builds main parts are:
 - Tracks 2.3.0 (stable)
 - Ubuntu 14.04 
 - Apache 2 (Passenger)
 - Sqlite3
 - Dockerize (Utility to simplify running applications in docker containers)

It utilizes mostly native Ubuntu 14.04 packages, thus rebuilding it will provide the latest updates.

Setting these docker environment variables will allow you to substitute you custom values into the templates at runtime:

TRACKS_TOKEN

TRACKS_DB

Example on how to run the Tracks container:

     docker run -d --name=tracks -e TRACKS_TOKEN=asdskldmwslkdafniowfno232233 -p 80:80 eyecreate/tracks


 

References:
http://www.getontracks.org/

