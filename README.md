# Shadowsocks Server Kit

by Freeman

# Requirements

Place all the files in this package into a directory called `shadowsocks` in your home folder. For example, `~/shadowsocks/README.md` or `/home/ubuntu/shadowsocks/README.md`.

You need a system that has Upstart installed. Ubuntu 14 LTS has this out of the box. NB: Ubuntu 15+ uses a different task system.

Install `go` (if not already installed). You can use this snippet on Ubuntu:
```
sudo add-apt-repository ppa:gophers/archive
sudo apt update
sudo apt-get install golang-1.9-go
```

# Steps to get this working

- Install go-shadowsocks2 by running `sh install-shadowsocks.sh`.

- Run `chmod +x shadowsocks-server-linux64-1.1.5`
- Edit `shadowsocks.conf` to point to this directory, and also replacing your username.
- **CHANGE THE PASSWORD** in `config.json`.
- Run `sudo cp shadowsocks.conf /etc/init/shadowsocks.conf`.
- You can now start Shadowsocks, with automatic crash recovery, with `sudo service shadowsocks start`.
- If you want to stop the service, or restart, you can run `sudo service shadowsocks stop`.
