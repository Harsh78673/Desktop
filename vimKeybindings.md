Here’s a **Vim command cheatsheet** that includes the most useful and commonly used commands for text editing in Vim. This cheat sheet will help you navigate
your file efficiently and manipulate text quickly.

---

### **Basic File Operations**
1. **u** - Move cursor to specified location or position (or cursor left/right/up/down)
   ```
   u x
   ```

2. **x** - Set cursor to the end of the screen.
   ```
   x
   ```

3. **y** - Move cursor vertically.
   ```
   y
   ```

4. **c** - Jump cursor to current character (or position) in the file or directory.
   ```
   c
   ```

5. **p** - Print output from command buffer while keeping cursor at specified location.
   ```
   p x
   ```

6. **m** - Move cursor to next selected item when in file mode or to current line otherwise.
   ```
   m
   ```

7. **t** - Toggle cursor mode (file vs line).
   - Use `t` with cursor at command buffer to print the output without moving.
   ```
   t
   ```

8. **s** - Save output from command buffer while keeping cursor at specified location.
   ```
   s x
   ```

---

### **Text Manipulation**
9. **l r u p y c m t s**:
   - Use these commands to manipulate text in the current file or directory.

#### Basic Operations:
- **i** - Insert a character at cursor position.
  ```
  i
  ```
- **d** - Delete the last character typed.
  ```
  d
  ```

#### String Operations:
10. **cat** - List contents of file, command buffer, and directory.
    ```
    cat "file.txt"
    cat /
    ```

11. **tr/td** - Trim whitespace from string or replace line breaks in a text file.
    ```
    tr ' \t\n\r' ''  # Trims spaces, tabs, newlines, etc.
    tr / \n       # Replaces backslashes with newlines (for multi-line strings)
    ```

12. **split** - Split text on a specified delimiter and save back to command buffer.
    ```
    split "a b c d" " "
    split "hello world" "?"
    ```

13. **format** - Format string and save result back into file or buffer.
    ```
    format "Hello %s World" % "This is my first line."
    format / % "This is my first line."
    ```

---

### **File Navigation**
14. **f p r l u y m t s**:
   - Use these commands to navigate through files in Vim.

#### File Mode:
15. **f f** (file mode): Switch between file, directory, and terminal.
    ```
    f f
    ```

#### Current File:
16. **f c** - Move cursor to current file item.
    ```
    f c
    ```

#### Selecting Items:
17. **f s** - Select next selection in the command buffer.
    ```
    f s
    ```

#### Current Directory:
18. **f d** - Toggle directory mode.
    ```
    f d
    ```

---

### **Advanced Features**
19. **q h n l m t p s z**:
   - Use these commands for command history and navigation.

#### Command History:
20. **h c** - Open command history to view context menu or list of previously executed commands.
    ```
    c q h
    ```

#### Previous Commands:
21. **prev** - Move cursor back to previous command in command buffer.
    ```
    prev
    ```

#### Next Command:
22. **next** - Move cursor to next command in command buffer (or end if at last one).
    ```
    next
    ```

---

### **Customization and Styling**
23. **u c 0 x**: Change cursor color to black and position to current character.
    ```
    u c 0 x
    ```

24. **d g**: Generate a default line width based on text in buffer or file.
    ```
    d g
    ```

---

### **Examples**
Here’s how you might use some Vim commands:

1. Print output to standard output:
   ```
   p <input>
   p -i "Hello, world!"
   ```

2. Trim whitespace from a line and save back:
   ```
   tr '  \t\n\r' ''
   ltr
   ```

3. Split text on a delimiter and save back:
   ```
   split "a b c d" " "
   ltr
   ```

4. Format a string with placeholders and save back:
   ```
   format %s %d "My date is %Y-%m-%d"
   #2023-12-05
   ```

---