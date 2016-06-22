# alpine-nginx-nodejs

A Docker image for running [nginx][nginx] with [Node.js][nodejs], based on Alpine Linux.
This image belongs to a suite of images [documented here][dockeralpine].

## Features

This image features:

- [Alpine Linux][alpinelinux]
- [s6][s6] and [s6-overlay][s6overlay]
- [consul][consul]

## Versions

- `2.1.1`, `latest` [(Dockerfile)](https://github.com/smebberson/docker-alpine/blob/master/alpine-nginx-nodejs/Dockerfile)
- `2.1.0` [(Dockerfile)](https://github.com/smebberson/docker-alpine/blob/bbdb320fed4c6453d1ea0065c9f0089d6a91c47f/alpine-nginx-nodejs/Dockerfile)
- `2.0.0` [(Dockerfile)](https://github.com/smebberson/docker-alpine/blob/40f6de779f5d2ea0ea3f5f36a8942aa49f238304/alpine-nginx-nodejs/Dockerfile)
- `1.0.0` [(Dockerfile)](https://github.com/smebberson/docker-alpine/blob/8df61b908df740450527265d48af98bbfd296245/alpine-nginx-nodejs/Dockerfile)

[See VERSIONS.md for image contents.](https://github.com/smebberson/docker-alpine/blob/master/alpine-nginx-nodejs/VERSIONS.md)

## Usage

To use this image include `FROM smebberson/alpine-nginx-nodejs` at the top of your `Dockerfile`. Inheriting from `smebberson/alpine-nginx-nodejs` provides you with the ability to run nginx, within a container that has Node.js for easy configuration.

The container will automatically start nginx for you. For information about how to customise the nginx setup, and where to put your static files [read the guide for smebberson/alpine-nginx][smebbersonalpinenginxgithub].

The contianer won't automatically start or manage your Node.js application. For information about how to set this up, [read the guide for smebberson/alpine-nodejs][smebbersonalpinenodejsgithub].

### Logging

nginx logs won't automatically stream to stdout. [Read the guide for smebberson/alpine-nginx][smebbersonalpinenginxgithub] to learn how to access the logs.

If Node.js application logs to stdout (which `console.log` does) then you'll be able to review your logs using the standard [Docker process][dockerlogs].

## Example

An example of using this image can be found in [examples/user-nginx-nodejs][example].

[dockeralpine]: https://github.com/smebberson/docker-alpine
[s6]: http://www.skarnet.org/software/s6/
[s6overlay]: https://github.com/just-containers/s6-overlay
[dockerlogs]: https://docs.docker.com/reference/commandline/cli/#logs
[alpinelinux]: https://www.alpinelinux.org/
[alpinebase]: (https://registry.hub.docker.com/u/smebberson/alpine-base/)
[smebbersonalpinenginx]: https://registry.hub.docker.com/u/smebberson/alpine-nginx/
[smebbersonalpinenodejs]: https://registry.hub.docker.com/u/smebberson/alpine-nodejs/
[smebbersonalpinenginxgithub]: https://github.com/smebberson/docker-alpine/tree/master/alpine-nginx
[smebbersonalpinenodejs]: https://github.com/smebberson/docker-alpine/tree/master/alpine-nginx
[example]: https://github.com/smebberson/docker-alpine/tree/master/examples/user-nginx-nodejs
[nodejs]: https://nodejs.org/
[nginx]: http://nginx.org/
