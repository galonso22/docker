# Docker

### Instalar docker

Ubuntu Trusty 14.04 (LTS) (64-bit)

```sh
$ sudo apt-get update
$ sudo apt-get install docker.io
```
Then, to enable tab-completion of Docker commands in BASH, either restart
BASH or:

```sh
$ source /etc/bash_completion.d/docker.io
```

## Instalar fig

>Fig is a python application that helps you run groups of docker containers. >The docker command line interface is awesome, but if you start working with >many containers at once and link them in the development environment, typing >the commands into the command line gets burdensome.

Ejecutar:
```sh
curl -L https://github.com/docker/fig/releases/download/1.0.1/fig-`uname -s`-`uname -m` > /usr/local/bin/fig; chmod +x /usr/local/bin/fig
```