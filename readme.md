# Docker SciRuby/IRuby Notebook

Get a working IRuby notebook inside of a Docker container.

Comes with:

- NMatrix

## Quickstart

1. Install [Docker](https://docker.com). I use
   [docker-machine](https://docs.docker.com/machine/) on my laptop.

2. Pull and run the SciRuby-Notebook image:

```sh
docker run \
  --publish=8888:8888 \
  --volume=$PWD/notebook:/notebooks \
  audy/sciruby-notebook
```

Point a browser to http://dockerhost:8888.

## Development

```sh
# assuming you have Docker working

git clone https://github.com/audy/docker-sciruby-notebook
cd docker-sciruby-notebook
docker build . # note image_id

# start the notebook
docker run \
  --publish=8888:8888 \
  --volume=$PWD/notebooks:/notebooks \
  $image_id
```

## LICENSE

Licensed under MIT. See license.md for details.

Contributions appreciated.
