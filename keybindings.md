# 📌 Zellij Commands

- ⌨️ `Ctrl + P` → Panel mode
- ➕ `Ctrl + P n` → New pane
- 📂 `Ctrl + P d` → Open terminal downwards
- 🔀 Move: `Alt + ⬆️⬇️⬅️➡️`
- 🆕 `Ctrl + T n` → New tab
- ✏️ `Ctrl + T r` → Rename tab
- 📏 Resize: `Alt + )` → Move side, `Alt + -` → Shrink, `Alt + +` → Expand
- ➡️ `Ctrl + A Shift + %` → Open pane right
- ⬇️ `Ctrl + A Shift + "` → Open pane down

---

# 📝 Neovim Commands

- 📂 `cd <dir> && n .` → Open Neovim in directory
- 📁 `Space e` → File explorer
- 🔍 `Space space` → Fuzzy finder
- ℹ️ `i` → File info in explorer

---

# 📸 Screenshot Commands

- 🖥️ `Print` → Open GNOME screenshot
- ⚙️ `Ctrl + Print` → More options

---

# 🛠️ Lazygit

- 🔧 `Space gg` → Open Lazygit

---

# 🖥️ Terminal Commands

- 📁 `yazi` → Terminal file explorer
- ❌ `q` → Quit Yazi
- 📜 `Ctrl + R` → Command history
- 🔍 `ls -l | grep <file>` → Search file
- 🚫 `rm -rf myvenv` → Permanent delete

---

# 📦 Installed Packages

- `sudo add-apt-repository ppa:oibaf/graphics-drivers`
- 🏗️ `stow`
- 🖥️ `yazi`, `lazygit`, `fzf`
- 🛠️ `open-vm-tools`, `github-cli (gh)`
- 🍺 `Homebrew`
- 🤖 `ollama` → `deepseekr1:1.5b -- 4bit`
- 📜 `tmux`, `vim-tmux-navigator`

---

# 🐍 Python Virtual Environment Setup

- 📥 `sudo add-apt-repository ppa:deadsnakes/ppa`
- 📦 `sudo apt install python3 -m venv <venv>`
- 🏗️ `sudo apt install python3.11 -m venv myvenv`
- ▶️ `source myvenv/bin/activate`
- ⏹️ `deactivate`

---

# 🤖 Ollama Commands

- 📜 `ollama list`
- 🚀 `ollama run deepseekr1:1.5b`

---

# 🔧 Set Vim h, j, k, l in Alacritty & Zellij

- ⚙️ `set -o vi`

---

# 📌 Zellij Commands

- 🛠️ `zelliji --help`
- 🔒 `Ctrl + G` → Lock Zellij panel (so tmux works properly)

---

# 🔄 Tmux Commands

- 🎛️ Leader key changed: `Ctrl + A`
- 🔄 `tmux source ~/.tmux.conf` → Reload config
- 🛠️ Plugins installed:
  - `christoomey/vim-tmux-navigator`
  - `tmux-plugins/tmux-resurrect`
- 🔒 `Ctrl + G` → Lock Zellij for Tmux

### 📂 Tmux Session Management

- 🎯 `tmux new-session -d -s my-session`
- 🏷️ `tmux attach-session -t my-session`
- 💾 `mod(Ctrl + A) S` → Save session
- 🔄 `mod(Ctrl + A) R` → Restore session
- ➕ `Ctrl + A c` → New window
- ⬅️➡️ `Ctrl + A ⬆️⬇️` → Switch window
- 📜 `tmux ls` → List sessions
- 🔌 `tmux attach-session -t <session>`
- 🚀 `tmux attach`
- 🔀 Resize with `Ctrl + B` then `Ctrl + Arrows`

### 🛠️ Custom Scripts (File Paths)
- **Save:** `~/scripts/save_tmux_session.sh`
- **Restore:** `~/scripts/restore_tmux_session.sh`
- **List:** `~/scripts/list_saved_sessions.sh`

### 🔧 Custom Keybindings (`.tmux.conf`)

```bash
# Save session: Ctrl + B + S
bind s run "bash ~/scripts/save_tmux_session.sh"

# Restore session: Ctrl + B + R
bind r run "bash ~/scripts/restore_tmux_session.sh"

# List saved sessions: Ctrl + B + L
bind l run "bash ~/scripts/list_saved_sessions.sh"
```

---

### 🚀 Best Practices for Tmux

- 📌 Start a named session: `tmux new-session -s mysession`
- 🔄 Reattach: `tmux attach-session -t mysession`
- 📏 Resize panes: `Ctrl + B` + `Ctrl + Arrow`
- 🔧 Install/uninstall plugins inside Tmux
- 🏗️ `tmux` again for a new session

