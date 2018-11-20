# Docker Debian Oracle JDK 11

[![Docker pulls](https://img.shields.io/docker/pulls/goodforgod/debian-jdk10-oracle.svg)](https://registry.hub.docker.com/v2/repositories/goodforgod/debian-jdk10-oracle/)
[![Docker Stars](https://img.shields.io/docker/stars/goodforgod/debian-jdk10-oracle.svg)](https://registry.hub.docker.com/v2/repositories/goodforgod/debian-jdk10-oracle/)
[![Docker Automated build](https://img.shields.io/docker/automated/goodforgod/debian-jdk10-oracle.svg?maxAge=31536000)](https://registry.hub.docker.com/v2/repositories/goodforgod/debian-jdk10-oracle/)

Docker Debian image with Oracle JDK 11.0.1 (247MB)

You must accept the [Oracle Binary Code License Agreement for Java SE](http://www.oracle.com/technetwork/java/javase/terms/license/index.html) to use this image.

## Usage

Image have docker *USER* named **app** so you can use it for your application.
Just add code below in your *Dockerfile*
```
USER app
```

Check [example](https://github.com/GoodforGod/https://github.com/GoodforGod/docker-debian-jre10server-oracle/tree/master/example) folder for *Dockerfile* example of image usage.

## Image
Image contains cleaned [Oracle JDK 11.0.1](http://www.oracle.com/technetwork/java/javase/downloads/jdk10-downloads-4416644.html). 
JDK is provided without *desktop, sources* and other unnecessary stuff except JVM and javac. Some tags have mission control included as well (check image section below).
Image have all *JVM* parts to run and compile *Java applications* in Docker containers.

If you **encountered such errors** when starting applications
```bash
java: /lib/x86_64-linux-gnu/libdl.so.2: version `GLIBC_2.2.5' not found (required by /opt/java/jdk-11.0.1/bin/../lib/jli/libjli.so)
java: /lib/x86_64-linux-gnu/libdl.so.2: version `GLIBC_2.2.5' not found (required by /lib/x86_64-linux-gnu/libpam.so.0)
```
Then use [**SID**](#sid) image tag.

## Tags

#### *latest* or *stretch*
* Uses base image [Debian Stretch Slim](https://hub.docker.com/_/debian/) *(55.3MB)*
* Image size with JDK *(247MB)*

```dockerfile
FROM goodforgod/debian-jdk11-oracle
```

#### *sid*
* Uses base image [Debian Sid Slim](https://hub.docker.com/_/debian/) *(63.3MB)*
* Image size with JDK *(266MB)*

```dockerfile
FROM goodforgod/debian-jdk11-oracle:sid
```

## Usage
Image have docker *USER* named **app** so you can use it for your application.

Just add code below in your *Dockerfile* to use start your application as a user *app*
```
USER app
```

Check [example](https://github.com/GoodforGod/https://github.com/GoodforGod/docker-debian-jdk11-oracle/tree/master/example) folder for *Dockerfile* example of image usage.
