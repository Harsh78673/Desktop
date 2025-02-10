# 🍺 Homebrew vs APT Cheatsheet

This cheatsheet helps you transition from `apt` commands to `brew` commands after installing Homebrew on your system.

## 📌 Basic Commands

| Action                         | APT Command                          | Brew Command               |
|--------------------------------|--------------------------------------|-----------------------------|
| Update package list            | `sudo apt update`                   | `brew update`              |
| Upgrade installed packages     | `sudo apt upgrade`                  | `brew upgrade`             |
| Install a package              | `sudo apt install <package>`        | `brew install <package>`   |
| Uninstall a package            | `sudo apt remove <package>`         | `brew uninstall <package>` |
| Search for a package           | `apt search <package>`              | `brew search <package>`    |
| List installed packages        | `apt list --installed`              | `brew list`                |
| Get package info               | `apt show <package>`                | `brew info <package>`      |
| Clean up old versions          | `sudo apt autoremove && apt clean`  | `brew cleanup`             |

## 🔍 Managing Services

| Action                         | APT Equivalent                      | Brew Command               |
|--------------------------------|--------------------------------------|-----------------------------|
| Start a service                | `sudo systemctl start <service>`    | `brew services start <service>`  |
| Stop a service                 | `sudo systemctl stop <service>`     | `brew services stop <service>`   |
| Restart a service              | `sudo systemctl restart <service>`  | `brew services restart <service>` |
| Check service status           | `sudo systemctl status <service>`   | `brew services list`       |

## 🛠️ Troubleshooting

| Issue                           | APT Fix                              | Brew Fix                   |
|----------------------------------|--------------------------------------|-----------------------------|
| Fix broken dependencies         | `sudo apt --fix-broken install`      | N/A                         |
| Check for missing dependencies  | `apt depends <package>`              | `brew deps <package>`       |
| Remove unnecessary packages     | `sudo apt autoremove`                | `brew autoremove`           |
| Reinstall a package             | `sudo apt reinstall <package>`       | `brew reinstall <package>`  |

## 🏗️ Working with Casks (GUI Apps)

Unlike APT, Brew has a `cask` feature for GUI applications.

| Action                         | APT Equivalent (if any)              | Brew Command               |
|--------------------------------|--------------------------------------|-----------------------------|
| Install GUI app                | `sudo apt install <app>` (if exists) | `brew install --cask <app>` |
| List installed GUI apps        | `apt list --installed`               | `brew list --cask`          |
| Uninstall GUI app              | `sudo apt remove <app>`              | `brew uninstall --cask <app>` |

## 📦 Managing Taps (Extra Repos)

APT uses PPAs; Brew uses Taps.

| Action                         | APT Command                          | Brew Command               |
|--------------------------------|--------------------------------------|-----------------------------|
| Add a new repository           | `sudo add-apt-repository ppa:repo`  | `brew tap <repo>`          |
| Remove a repository            | `sudo add-apt-repository --remove`  | `brew untap <repo>`        |
| List all repositories          | `ls /etc/apt/sources.list.d/`       | `brew tap`                 |

## 🔗 Useful Links

- [Homebrew Documentation](https://brew.sh)
- [APT User Guide](https://help.ubuntu.com/community/AptGet/Howto)

🎯 **Now you're ready to use Homebrew like a pro! 🚀**

