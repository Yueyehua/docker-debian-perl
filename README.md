debian-perl
===========

This is a Debian Jessie docker image with perl and plenv installed.

Prerequisites
-------------

- Docker

Usage
-----

```text
docker pull yueyehua/debian-perl
docker run \
  -d \                                           # daemonize
  --privileged \                                 # for systemd
  -v /sys/fs/cgroup:/sys/fs/cgroup:ro \          # for systemd
  --name perl \                                  # container name
  -h perl \                                      # hostname
  yueyehua/debian-perl
docker exec -ti perl bash
[Do something here]
docker stop perl
docker rm perl
```
