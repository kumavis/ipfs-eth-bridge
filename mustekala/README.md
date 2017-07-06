# Mustekala Box

## Overview

Designed to operate on a coreOS box with default configs.
This is a full functioning set of containers running a reverse proxy in `443`,
with forwarding from `80` to the `ws` port in the IPFS bridge, which has
a read only parity-ipfs datastore.

The generation of SSL certificates is made with `Let's encrypt` automatically.

## Requirements

Install `docker-compose`

```
mkdir -p /opt/bin
curl -L "https://github.com/docker/compose/releases/download/1.14.0/docker-compose-$(uname -s)-$(uname -m)" -o /opt/bin/docker-compose
chmod +x /opt/bin/docker-compose
```

## Execution

* Download this repository
* cd <this repository>/mustekala
* `./run_box`

## Customization

Just change the environmental variables in `mustekala/docker-compose.yml`
to your own domain, subdomains and admin email.
