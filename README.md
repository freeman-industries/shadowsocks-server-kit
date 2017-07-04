# Shadowsocks Server Kit

by Freeman

# Steps to get this working

- Ensure you are running on a server that supports Upstart. Ubuntu 14 does, 15+ does not.
- Make sure all these files are in a directory called `shadowsocks` in your home folder. For example, `~/shadowsocks/README.md` or `/home/ubuntu/shadowsocks/README.md`.
- Run `chmod +x shadowsocks-server-linux64-1.1.5`
- Edit `shadowsocks.conf` to point to this directory, and also replacing your username.
- **CHANGE THE PASSWORD** in `config.json`.
- Run `sudo cp shadowsocks.conf /etc/init/shadowsocks.conf`.
- You can now start Shadowsocks, with automatic crash recovery, with `sudo service shadowsocks start`.
- If you want to stop the service, or restart, you can run `sudo service shadowsocks stop`.
