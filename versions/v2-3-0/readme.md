Build with:

```
docker build --tag 'tracks-2-3-0' .
```

Then run it:

```
docker run -p 80:80 "tracks-2-3-0"
```

or

```
docker run -d --name=tracks -p 80:80 "tracks-2-3-0"
```

Then visit:

http://localhost:80

Create an admin user e.g. admin/password

Then login and use the API.

If you find that you can't login or can't create an admin session then try opening the link in incognito mode... if that works then delete the "_tracksapp_session" cookie in your normal browser window.
