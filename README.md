nodejs-nginx
==================

You don't need to use node to serve any node based site - you can and should use nginx when possible.

This is a container that has node and nginx available.

You can use our container: `docker pull octohost/nodejs-nginx`

Or you can build your own:

```
docker build -t your-name-here/nodejs-nginx .
docker push your-name-here/nodejs-nginx
```

After this - just add this Dockerfile to your Node repo:

```
FROM octohost/nodejs-nginx

WORKDIR /srv/www

ADD . /srv/www/
RUN install your node modules here
RUN compile your site here.

EXPOSE 80

CMD nginx
```
