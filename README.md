# kali
A Docker image for various bits of Kali Linux

[![](https://images.microbadger.com/badges/image/brimstone/kali.svg)](https://microbadger.com/images/brimstone/kali "Get your own image badge on microbadger.com")
[![](https://img.shields.io/docker/stars/brimstone/kali.svg)](https://hub.docker.com/r/brimstone/kali 'DockerHub')

## Basic Usage
`docker run --rm -ti --net host brimstone/kali msf`

This will start `msfconsole` with a postgresql server, ready to rock. The
postgresql server has already been preloaded with the module cache, so lookups
should be fast.

## Advanced Usage

There's a number of other fun tools in here:

### zaproxy
`docker run --rm -it --net host -e DISPLAY=unix$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix brimstone/kali zaproxy`

### armitage
`docker run --rm -it --net host -e DISPLAY=unix$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix brimstone/kali armitage`

### good ol' bash
`docker run --rm -it --net host brimstone/kali`
