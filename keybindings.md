# Zellij Commands

- `ctrl+p` to go to panel mode, then `ctrl+p n` for a new pane
- `ctrl+p` and then `d` to open a new terminal downwards
- Move around with `alt + up`, `down`, `left`, `right` arrows
- `ctrl+t` then `n` to open a new tab
- `ctrl+t r` to rename the tab
- `alt + )` to move terminal to the side
- `alt + -` to make it smaller and `alt + +` to make it larger
- `ctrl+a` then `shift + %` to open terminal pane on the right
- `ctrl+a` then `shift + "` to open terminal pane down

---

# Neovim Commands

- To open Neovim in a directory, `cd` there then press `n .` to open Neovim in that directory
- `space e` to open file explorer
- `space space` to open fuzzy finder
- `i` to get info about the file you are in file explorer

---

# Screenshot Commands

- `print` to open Gnome screenshot
- `ctrl + print` for more options

---

# Lazygit

- `space gg` to open Lazygit

---

# Terminal Commands

- `yazi` - terminal file explorer
- `q` to quit yazi
- `ctrl+r` for terminal commands history
- `ls -l | grep <file name>` to search for a file
- `rm -rf myvenv` to remove something or a package permanently

---

# Installed Packages

- `sudo add-apt-repository ppa:oibaf/graphics-drivers`
- `Omakub`
- `stow`
- `yazi`
- `lazygit`
- `fzf`
- `open-vm-tools`
- `github-cli` => `gh`
- `Homebrew` or `brew` and its build essentials
- `ollama` -> `deepseekr1:1.5b -- 4bit`
- `tmux`
- `tmux plugin manager (tpm)`
- `vim-tmux-navigator` in Neovim

---

# Steps to Install Python Virtual Environment

- `sudo add-apt-repository ppa:deadsnakes/ppa` -> for latest and old versions of Python
- `sudo apt install python3 -m venv <name of your venv>`
- `sudo apt install python3.11 -m venv myvenv`
- `source myvenv/bin/activate` -> to activate the venv
- `deactivate` -> to deactivate venv

---

# Ollama Commands

- `ollama list`
- `ollama run deepseekr1:1.5b`

---

# Set Vim h, j, k, l in Alacritty & Zellij

- `set -o vi`

---

# Zellij Commands

- `zelliji --help`
- `ctrl+g` to lock Zellij panel so tmux could work properly

---

# Tmux Commands

- **Default leader key in tmux is `ctrl+b`**
- **Leader changed to `ctrl+a`**

- After changing anything in `tmux.conf` file, run `tmux source ~/.tmux.conf`
- **Tmux plugins installed:**

  - `set -g @plugin 'christoomey/vim-tmux-navigator'`
  - `set -g @plugin 'tmux-plugins/tmux-resurrect'`

- `ctrl+g` to lock Zellij panel so tmux could work properly
- **Now `ctrl+b` is `ctrl+a` in tmux**

- `tmux new-session -d -s my-session`
- `tmux attach-session -t my-session`

**Tmux Session Commands to Save and Restore**

- `mod(ctrl+a)` then `S` to save a session (It will only restore the last session before shutting down the system)
- `mod(ctrl+a)` then `R` to restore the last session before shutdown

- `ctrl+a` then `c` to create a new window
- `ctrl+a` then `n` to switch to the previous window (you can also type `ctrl+a` then the number of the window)
- `ctrl+a` then `%` to split the pane vertically to the left
- `ctrl+a` then `"` to split the pane horizontally down
- To move through these windows, `ctrl+a` then arrow keys or `alt+arrow keys`
- `ctrl+a` then `:` to open command mode in tmux
- In command mode, type `rename-window name` to change the name of the window you are in
- `ctrl+a` then `:` then `rename-session nameSession`
- `ctrl+a` then `d` to detach from tmux
- `tmux ls` to list the sessions that you have open in tmux
- `tmux attach-session -t <session-name>`
- `tmux attach-session -t 0` to attach to the session with ID 0
- `tmux attach` to attach to the session again
- For a new session, detach from the current session then `tmux` again
- `ctrl+a` then `s` will list all the sessions inside tmux, then you can go up and down and press enter

**Start a Named Tmux Session (Best Practice)**

To keep your session organized:

- `tmux new-session -s mysession`

Then, later, you can reattach to it:

- `tmux attach-session -t mysession`

**Easier Way: Use Arrow Keys to Resize**

Instead of typing commands, you can hold a key combination and use arrow keys:

Press:

- `Ctrl + b`, then hold `Ctrl` and press an arrow key
  - `Ctrl + b → Ctrl + Left` → Shrink pane left
  - `Ctrl + b → Ctrl + Right` → Grow pane right
  - `Ctrl + b → Ctrl + Up` → Grow pane up
  - `Ctrl + b → Ctrl + Down` → Shrink pane down

**You need to be inside tmux to install or uninstall tmux plugins**

# Tmux Session Management

This guide provides commands and instructions for saving, restoring, and listing tmux sessions using custom scripts.

## Prerequisites

- **Scripts**:
  - `save_tmux_session.sh` to save tmux sessions.
  - `restore_tmux_session.sh` to restore tmux sessions.
  - `list_saved_sessions.sh` to list saved tmux sessions.

### **File Paths**
- Save Script: `~/scripts/save_tmux_session.sh`
- Restore Script: `~/scripts/restore_tmux_session.sh`
- List Script: `~/scripts/list_saved_sessions.sh`

### **Tmux Keybindings**
To make using these scripts more convenient, add the following keybindings to your `.tmux.conf`:

```bash
# Bind Ctrl-b + s to save tmux session (calls save_tmux_session.sh)
bind s run "bash ~/scripts/save_tmux_session.sh"

# Bind Ctrl-b + r to restore tmux session by name (calls restore_tmux_session.sh)
bind r run "bash ~/scripts/restore_tmux_session.sh"

# Bind Ctrl-b + l to list saved tmux sessions (calls list_saved_sessions.sh)
bind l run "bash ~/scripts/list_saved_sessions.sh"

