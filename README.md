# graph-explorer-docker

builds the [vimeo/graph-explorer](https://registry.hub.docker.com/u/vimeo/graph-explorer) docker image,
to easily deploy [Graph-Explorer](http://vimeo.github.io/graph-explorer/)

# building

* install docker on your system
* make a new directory, cd into it and put your own Dockerfile in it, it looks like so:

```
FROM vimeo/graph-explorer
```

* put a customized config.cfg in the directory

* make a directory in it called 'plugins', this will become available under /opt/graph-explorer/plugins
  Even when you don't have any custom plugins, this directory should exist (it's a docker thing, sorry)
  When you do, you can put them there and reference them from your config.

```
docker build .
```

* run !

```
docker run <image-id>
```
