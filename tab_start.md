---
title: Start
layout:  null
tab: true
order: 1
tags: webgoat
---

## Getting started

### 1. Standalone 

Download the latest WebGoat release from [https://github.com/WebGoat/WebGoat/releases](https://github.com/WebGoat/WebGoat/releases)

```Shell
java -jar webgoat-server-8.0.0.VERSION.jar [--server.port=8080] [--server.address=localhost]
```

The latest version of WebGoat needs Java 11. By default WebGoat starts on port 8080 with `--server.port` you can specify a different port. With `server.address` you
can bind it to a different address (default localhost)


### 2. Run using Docker

Every release is also published on [DockerHub](https://hub.docker.com/r/webgoat/webgoat-8.0/).

```Shell
docker pull webgoat/webgoat-8.0
docker run -p 8080:8080 -t webgoat/webgoat-8.0
```

### 3. Using docker-compose

The easiest way to start WebGoat as a Docker container is to use the `docker-compose.yml` [file](https://raw.githubusercontent.com/WebGoat/WebGoat/develop/docker-compose.yml) 
from our Github repository. This will start both containers and it also takes care of setting up the
connection between WebGoat and WebWolf.

```shell
curl https://raw.githubusercontent.com/WebGoat/WebGoat/develop/docker-compose.yml | docker-compose -f - up
```

**Important**: the current directory on your host will be mapped into the container for keeping state.

Using the `docker-compose` file will simplify getting WebGoat and WebWolf up and running.

### Running

Once started point your browser to `http://localhost:8080/WebGoat` to open WebGoat
