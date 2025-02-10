# Vim Commands Cheatsheet

## 🧭 Navigation

- **←** `h` → Move left
- **↓** `j` → Move down
- **↑** `k` → Move up
- **→** `l` → Move right
- **⟸** `0` → Move to the beginning of the line
- **⟸** `^` → Move to the first non-blank character of the line
- **⟹** `$` → Move to the end of the line
- **▲** `gg` → Go to the beginning of the file
- **▼** `G` → Go to the end of the file
- **⏩** `w` → Move to the start of the next word
- **⏪** `b` → Move to the beginning of the previous word
- **👇** `ctrl + f` → Move forward one page
- **👆** `ctrl + b` → Move backward one page
- `Ctrl + u` → Scroll up half a page
- `Ctrl + d` → Scroll down half a page

## ✏️ Editing

- **📝** `i` → Insert before the cursor
- **📝** `I` → Insert at the beginning of the line
- **📝** `a` → Append after the cursor
- **📝** `A` → Append at the end of the line
- **📝** `o` → Open a new line below
- **📝** `O` → Open a new line above
- **❌** `x` → Delete the character under the cursor
- **❌** `dd` → Delete the current line
- **❌** `d$` → Delete from the cursor to the end of the line
- **❌** `d0` → Delete from the cursor to the beginning of the line
- **❌** `d3j` → Delete 3 lines down
- **❌** `d4k` → Delete 4 lines up
- **📋** `y` → Yank (copy) the selected text
- **📋** `p` → Paste the yanked text after the cursor
- **📋** `P` → Paste the yanked text before the cursor
- **↩️** `u` → Undo the last change
- **↪️** `Ctrl + r` → Redo the last undone change
- **▶️** `>>` → Indent the current line
- **◀️** `<<` → Un-indent the current line
- `J` → Join lines together
- **⌫** `Ctrl + h` → Delete the character before the cursor (backspace)

## 🔍 Search & Replace

- **🔍** `/pattern` → Search for a pattern
- `?pattern` → Search backward for a pattern
- **⏩** `n` → Go to the next occurrence
- **⏪** `N` → Go to the previous occurrence
- `:%s/old/new/g` → Replace all occurrences of `old` with `new` in the entire file
- `:s/old/new/g` → Replace all occurrences of `old` with `new` in the current line
- `:%s/old/new/gc` → Replace all occurrences with confirmation

## 🛠️ Miscellaneous

- **💾** `:w` → Save the file
- **🚪** `:q` → Quit Vim
- **💾** `:wq` → Save and quit
- **💾** `:x` → Save and quit
- **🚪** `:q!` → Quit without saving
- `:e <filename>` → Open a file
- `:set number` → Show line numbers
- `:set nonumber` → Hide line numbers
- **❓** `:help <command>` → Get help for a command
- `:split` → Split the window horizontally
- `:vsplit` → Split the window vertically
- `Ctrl + w` → Switch between open windows
- `:tabnew` → Open a new tab
- `:tabn` → Switch to the next tab
- `:tabp` → Switch to the previous tab
- `:bnext` → Switch to the next buffer
- `:bprev` → Switch to the previous buffer

## 🔢 Arrow + Number Delete Bindings

- `4j d` → Delete 4 lines down
- `3k d` → Delete 3 lines up
- `2h d` → Delete 2 characters to the left
- `5l d` → Delete 5 characters to the right

## 🎨 Icons (For Visual Appeal)

- :arrow_down: Move Down
- :arrow_up: Move Up
- :arrow_left: Move Left
- :arrow_right: Move Right
- :wrench: Edit
- :scissors: Delete
- :clipboard: Copy/Yank
- :pencil: Insert
- :recycle: Undo/Redo
- :search: Search
- :books: Help
- :fire: Execute
