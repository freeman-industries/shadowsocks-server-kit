# Shadowsocks Server Kit

by Freeman

# Requirements

This software is designed to be installed onto a Ubuntu 14.04 LTS system. You can use a different UNIX system, but the steps for installing all dependencies will vary.

- Git (`sudo apt install git`)
- Upstart (warning: not available on Ubuntu 15+)
- Shadowsocks-libev (`sudo apt install shadowsocks-libev`)

Place all the files in this package into a directory called `shadowsocks` in your home folder. For example, `~/shadowsocks/README.md` or `/home/ubuntu/shadowsocks/README.md`.

# Steps to get this working



- Install go-shadowsocks2 by running `GOPATH=$(readlink -e ./) go get -u -v github.com/shadowsocks/go-shadowsocks2`. Run this in the working directory (assumed `~/shadowsocks`).

- Run `chmod +x shadowsocks-server-linux64-1.1.5`
- Edit `shadowsocks.conf` to point to this directory, and also replacing your username.
- **CHANGE THE PASSWORD** in `config.json`.
- Run `sudo cp shadowsocks.conf /etc/init/shadowsocks.conf`.
- You can now start Shadowsocks, with automatic crash recovery, with `sudo service shadowsocks start`.
- If you want to stop the service, or restart, you can run `sudo service shadowsocks stop`.
