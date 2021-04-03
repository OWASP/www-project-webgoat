---
title: Start
layout:  null
tab: true
order: 1
tags: webgoat
---

## Getting started


### 1. Run using Docker

The easiest way to start WebGoat as a Docker container is to use the all-in-one Docker container. This is a Docker image that has WebGoat and WebWolf running inside.

```Shell
docker run -p 8080:8080 -p 9090:9090 -p 80:8888 -e TZ=Europe/Amsterdam webgoat/goatandwolf:latest
```

and browse to http://localhost:8080/WebGoat.

## 2. Standalone

Download the latest WebGoat and WebWolf release from [https://github.com/WebGoat/WebGoat/releases](https://github.com/WebGoat/WebGoat/releases)

```Shell
java -jar webgoat-server-8.1.0.jar [--server.port=8080] [--server.address=localhost]
java -jar webwolf-8.1.0.jar [--server.port=9090] [--server.address=localhost]
```

and browse to http://localhost:8080/WebGoat

The latest version of WebGoat needs Java 15 or above. By default, WebGoat uses port 8080, the database uses 9000 and WebWolf use port 9090 with the environment variable `WEBGOAT_PORT`, `WEBWOLF_PORT` and `WEBGOAT_HSQLPORT` you can set different values.

```Shell
export WEBGOAT_PORT=18080
export WEBGOAT_HSQLPORT=19001
export WEBWOLF_PORT=19090
java -jar webgoat-server-8.1.0.jar
java -jar webwolf-8.1.0.jar 
```

Use `set` instead of export on Windows cmd. 
