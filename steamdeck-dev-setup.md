# Steamdeck as a backup device

for dev

**Platform:** SteamOS (Steam Deck) - KDE Plasma 5 `plasmashell --version`

**Goal:** Full Ubuntu dev environment with VS Code and Git, Keep SteamOS as main OS for gaming features

**Method:** Distrobox (Ubuntu 24.04 container without GUI)

**Doc:** https://distrobox.it/

---

## **Background**
- SteamOS has **read-only root filesystem**
- **Distrobox** solves this problem, running Ubuntu container with full right at root
- Projects are stored in '~/Workspace' in Home which won't be gone after SteamOS update


---

## Quick Reference

### Distrobox : container

Distrobox installation
```bash
curl -s https://raw.githubusercontent.com/89luca89/distrobox/main/install | sh -s -- --prefix ~/.local
```

Check version
```bash
distrobox --version
```

Dostrobox commands

| Purpose | Command |
|---|---|
| list all | `distrobox list` |
| create | `distrobox create --name container-name --image ubuntu:24.04 --hostname host-name` |
| enter | `distrobox enter container-name` |
| exit | `exit` |
| stop | `distrobox stop container-name` |
| remove | `distrobox rm container-name` |



## Ubuntu : system

| Purpose | Command | Remark |  
|---|---|---|
| update packages | `sudo apt update && sudo apt upgrade -y` | -y yes to all | 
| show packages | `dpkg --list` | Debian PacKaGes |
| search a package | `dpkg --list , grep git` | Pipe inbetween |
| disk space | `df -h` | Disk Free Human readable |
| disk usage| `du -sh ~/` | Disk Usage -Summary -Human-readable |
| TOP10 disk usage| `du -sh ~/* , sort -rh , head -10` | Pipe inbetween |
| what installed via apt | `du -sh ~/` | without its dependencies|

Space in Home (all app files)
```
Filesystem      Size  Used Avail Use%  Mounted on
/dev/nvme0n1p8  512G  120G  392G  24%  /home```
```

---

### Ubuntu : software 

wget install
```bash
sudo apt install -y wget gpg
```

download and convert Microsoft Key
```bash
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
```

VS Code install
```bash
sudo apt update && sudo apt install -y code
```

turn off KWallet warning (Password Manager of KDE)
```bash
echo "--password-store=basic" >> ~/.var/app/com.visualstudio.code/config/code-flags.conf
```
