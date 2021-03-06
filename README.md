# README

Set of files for protecting Docker daemon socket

⚠️ This project is no longer maintained. ⚠️

## Installation

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/bin

# Use local installation

sudo bin/installer install

# Use remote installation

curl --location "https://gitlab.com/mauchede/docker-certificates/raw/master/bin/installer" | sudo sh -s -- install
```

__Note__: If you do not define `INSTALL_DIRECTORY`, `installer` will use in `/usr/local/bin`.

## Usage

```sh
export SSL_SIZE=4096
export SSL_SUBJECT=my-server.com

mkdir -p "${HOME}/.docker/certs/my-server"
sh -c "cd '${HOME}/.docker/certs/my-server' && bin/generate-certs"
```

__Note__: Available environment variables are listed in [OMGWTFSSL's README](https://github.com/paulczar/omgwtfssl#advanced-usage).

## Credits

The used script has been created by [paulczar](https://github.com/paulczar).

## Links

* [configure tls](https://docs.docker.com/swarm/configure-tls/)
* [paulczar/omgwtfssl](https://github.com/paulczar/omgwtfssl)
* [protect the docker daemon socket](https://docs.docker.com/engine/security/https/)
* [timonier/dumb-entrypoint](https://gitlab.com/timonier/dumb-entrypoint)
* [using ssl with an ip address instead of dns](https://bowerstudios.com/node/1007)
