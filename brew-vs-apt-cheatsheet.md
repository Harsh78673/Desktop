# Homebrew vs APT Cheatsheet

## 📌 Basic Package Management

| Task                        | APT Command                  | Brew Command               |
| --------------------------- | ---------------------------- | -------------------------- |
| Update package lists        | `sudo apt update`            | `brew update`              |
| Upgrade all packages        | `sudo apt upgrade`           | `brew upgrade`             |
| Install a package           | `sudo apt install <package>` | `brew install <package>`   |
| Uninstall a package         | `sudo apt remove <package>`  | `brew uninstall <package>` |
| List installed packages     | `apt list --installed`       | `brew list`                |
| Show package info           | `apt show <package>`         | `brew info <package>`      |
| Check for outdated packages | `apt list --upgradable`      | `brew outdated`            |
| Remove unused dependencies  | `sudo apt autoremove`        | `brew cleanup`             |

## 🔍 Searching for Packages

| Task                      | APT Command                    | Brew Command            |
| ------------------------- | ------------------------------ | ----------------------- |
| Search for a package      | `apt search <package>`         | `brew search <package>` |
| Show package dependencies | `apt-cache depends <package>`  | `brew deps <package>`   |
| Show reverse dependencies | `apt-cache rdepends <package>` | `brew uses <package>`   |

## 🛠 Troubleshooting & System Maintenance

| Task                           | APT Command                     | Brew Command              |
| ------------------------------ | ------------------------------- | ------------------------- |
| Check system for issues        | `sudo apt check`                | `brew doctor`             |
| Show package installation path | `dpkg -L <package>`             | `brew --prefix <package>` |
| Fix broken dependencies        | `sudo apt --fix-broken install` | `brew missing`            |

## 🔄 Managing Services

| Task                  | APT Command                           | Brew Command                      |
| --------------------- | ------------------------------------- | --------------------------------- |
| Start a service       | `sudo systemctl start <service>`      | `brew services start <service>`   |
| Stop a service        | `sudo systemctl stop <service>`       | `brew services stop <service>`    |
| Restart a service     | `sudo systemctl restart <service>`    | `brew services restart <service>` |
| List running services | `systemctl list-units --type=service` | `brew services list`              |

## 📦 Managing Repositories

| Task                | APT Command                                   | Brew Command        |
| ------------------- | --------------------------------------------- | ------------------- |
| Add a repository    | `sudo add-apt-repository ppa:<repo>`          | `brew tap <repo>`   |
| Remove a repository | `sudo add-apt-repository --remove ppa:<repo>` | `brew untap <repo>` |
| List repositories   | `apt policy`                                  | `brew tap`          |

### 📝 Notes:

- Homebrew installs software in `~/.linuxbrew` (for Linux) or `/usr/local` (for macOS), while APT installs system-wide.
- Homebrew often provides newer versions of software than APT.
- Use `brew doctor` to check for potential issues.

💡 **Tip:** If you're switching from APT to Brew, always check if the package is available using `brew search <package>` first!
