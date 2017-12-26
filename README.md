# Shadowsocks Server Kit

by Freeman

# Requirements

This software is designed to be installed onto a Ubuntu 16.10 LTS system. You can use a different UNIX system, but the steps for installing all dependencies will vary.

Remember to run `sudo apt update` first on a fresh server.

- Shadowsocks-libev (`sudo apt install shadowsocks-libev`)

# Steps to get this working

- **CHANGE THE PASSWORD** in `config.json`.
- Run `sudo cp config.json /etc/shadowsocks-libev/config.json`.
- You can now start Shadowsocks with `sudo systemctl start shadowsocks-libev`.
- If you want to stop the service, or restart, you can run `sudo systemctl stop shadowsocks-libev`.

# Connecting

Use any Shadowsocks client for your platform.

When connecting, ensure the port and encryption methods match `config.json`.

By default, the port is `443` and the encryption method is `chacha20-ietf-poly1305`.
