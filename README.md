# 🔔 cli-mupd — CLI Utility for Updating Local Mirrorlists with Ease

**cli-mupd** is a command-line tool designed to simplify the process of updating local package mirror lists or other similar configuration files. It's useful for Linux users and system administrators who need to maintain up-to-date and geographically optimal mirrors on systems like Arch Linux.

---

## ✅ Features

* Simple and intuitive CLI interface
* Automatically fetches the latest mirror lists
* Supports filtering mirrors by country, status, or protocol
* Backup of old mirrorlist before update
* Customizable via flags and config files
* Can work in automated scripts or cron jobs

---

## 🔧 Installation

### Arch Linux (AUR)

```bash
yay -S cli-mupd
```

Or using `git` and `makepkg`:

```bash
git clone https://aur.archlinux.org/cli-mupd.git
cd cli-mupd
makepkg -si
```

### Ubuntu / Debian

```bash
sudo apt install git build-essential
git clone https://github.com/username/cli-mupd.git
cd cli-mupd
make
sudo cp cli-mupd /usr/local/bin/
```

### Fedora

```bash
sudo dnf install git make gcc
git clone https://github.com/username/cli-mupd.git
cd cli-mupd
make
sudo cp cli-mupd /usr/local/bin/
```

---

## 🚀 Basic Usage

Update the mirrorlist using default settings:

```bash
cli-mupd
```

Specify a country (e.g., Germany):

```bash
cli-mupd -c DE
```

Backup mirrorlist before updating:

```bash
cli-mupd --backup
```

---

## ⚙️ Configuration

`cli-mupd` accepts several command-line options:

| Option            | Description                                                       |
| ----------------- | ----------------------------------------------------------------- |
| `-c`, `--country` | Filter mirrors by country code (e.g., `US`, `DE`, `UA`)           |
| `--https`         | Only use mirrors that support HTTPS                               |
| `--ipv6`          | Prefer IPv6 mirrors                                               |
| `--backup`        | Backup current mirrorlist before writing new one                  |
| `--path`          | Path to the mirrorlist file (default: `/etc/pacman.d/mirrorlist`) |
| `-h`, `--help`    | Show help message                                                 |

You can create a config file at `~/.config/cli-mupd/config.toml` for persistent settings.

---

## 🎯 Examples

### Update with German mirrors over HTTPS

```bash
cli-mupd -c DE --https
```

### Automatically backup before update

```bash
cli-mupd --backup
```

### Update mirrorlist using config file preferences

```bash
cli-mupd
```

---

## 📚 More Info

* Manual:

```bash
cli-mupd --help
```

* GitHub repository: [https://github.com/username/cli-mupd](https://github.com/username/cli-mupd)
* Arch Wiki (for mirrorlist management): [https://wiki.archlinux.org/title/Mirrors](https://wiki.archlinux.org/title/Mirrors)

---

## 🧩 Alternatives

* `reflector` — Popular Arch Linux mirror manager
* `rankmirrors` — Tool for ranking mirrors by speed
* `netselect` — Choose the fastest mirror automatically
