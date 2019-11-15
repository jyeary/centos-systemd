# Centos 7 with systemd
To build the image
`docker build --rm -t centos-systemd:7 .`

In order to run image on a mac you need to add some additional parameters.

    docker run -d -e=container=docker --stop-signal=SIGRTMIN+3 --tmpfs /tmp --tmpfs /run -v /sys/fs/cgroup:/sys/fs/cgroup:ro centos-systemd:7

## References
[1] [Systemd integration](https://github.com/docker-library/docs/tree/master/centos#systemd-integration)

[2] [Running systemd in a non-privileged container](https://developers.redhat.com/blog/2016/09/13/running-systemd-in-a-non-privileged-container/)

[3] https://github.com/moby/moby/issues/9950#issuecomment-442713669
