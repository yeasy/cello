hero: All concepts related to cello

# Concepts

## Server

### Components

*Components* are all the containers you need to run a Cello Server.

#### API Engine

Api engine supply the core function, all operations through the api service.

Host path mappings:

* /opt/cello/api-engine/media:/var/www/media {>>store all media files<<}
* /var/run/docker.sock:/var/run/docker.sock {>>Used for agent containers launch, which will deploy fabric, eg. network<<}
* (==optional==) $ROOT_PATH/src/api-engine:/var/www/server {>>When run in debug mode, MODE=dev, will mapping the source code into container, ROOT_PATH is the source code path.<<}

#### Postgres

Store all the data in postgres database, and the storage path is mapping out on the host.

Host path mappings:

* /opt/cello/postgres:/var/lib/postgresql/data {>>Store all db data.<<}

#### Dashboard

The Web UI of Cello.

## Agent

### Kubernetes

### Fabric Operator

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
```
