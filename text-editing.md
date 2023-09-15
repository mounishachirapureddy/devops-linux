# Learn File Editing Tools 📝💻

In this document, we will explore two popular terminal-based text editors: Vim and Nano. These editors are essential for file manipulation and text editing in Unix-like operating systems. We will cover basic commands for each editor, including opening a file, finding a string, making text modifications, and saving or closing files.

## 1. Learn Vim ✒️

In Vim, there are three primary modes of operation: Command mode, Insert mode, and Extended mode (also known as Visual mode). Each mode serves a distinct purpose and allows you to perform different tasks within the text editor. Here's a detailed description of each mode along with their use cases:

1. **Command Mode:**
   - **Description:** Command mode is the default mode when you open a file in Vim. In this mode, you can navigate through your document, perform text manipulation, and execute various commands.
   - **Use Cases:**
     - **Text Manipulation:** You can delete, copy, paste, and manipulate text using commands like `d` (delete), `y` (yank/copy), `p` (paste), `x` (cut), and `u` (undo).
     - **Searching:** You can search for text patterns using `/` (forward search) and `?` (backward search) followed by the search query.
     - **Saving and Quitting:** You can save changes with `:w` and quit Vim with `:q`. Combining them as `:wq` saves and quits, or you can force quit with `:q!`.

2. **Insert Mode:**
   - **Description:** In Insert mode, you can directly input and edit text as you would in a typical text editor. Vim switches to this mode when you press `i` (insert before cursor) in Command mode.
   - **Use Cases:**
     - **Typing and Editing:** Use Insert mode to add, modify, or delete text. You can type freely, just like in any other text editor.
     - **Inserting Text:** For inserting new text at specific locations within your document, press `i` or `a` to enter Insert mode at the desired position.

3. **Extended Mode (Visual Mode):**
   - **Description:** Extended mode, often referred to as Visual mode, allows you to visually select text in your document. It can be used to perform various operations on selected text, such as copying, cutting, and formatting.
   - **Use Cases:**
     - **Copy/Cut/Paste:** Once text is selected, you can copy it with `y` (yank), cut it with `x` (cut), or delete it with `d` (delete). Pasting is done with `p` (paste).
     - **Search and Replace:** Select text visually, and then use `:s` followed by a replacement command to perform find-and-replace operations on the selected text.

### 1.1. Installation of Vim on Ubuntu 🐧

You can install Vim on Ubuntu using the following command:

```bash
$ sudo apt update
$ sudo apt install vim -y
```

### 1.2. Installation of Vim on CentOS 🐧

To install Vim on CentOS, use the following command:

```bash
$ sudo yum install vim -y
```

### 1.3. Open a File in Vim 📂

To open a file in Vim, follow these steps:

```bash
$ vim filename
```

- **Example:** Open a file named "example.txt" in Vim.

  ```bash
  $ vim example.txt
  ```

### 1.4. Finding a String in Vim 🔍

You can search for a string within a file using Vim by pressing `/` followed by the string you want to find and then pressing Enter. To find the next occurrence, press `n`, and to find the previous occurrence, press `N`.

- **Example:** Search for the word "search" in the file.

  ```bash
  /search
  ```

### 1.5. Search and Replace in Vim 🔍🔄

To search and replace a single word, use the following command:

```bash
:%s/oldword/newword/g
```

### 1.6. Set Line Numbers in Vim 📊

To display line numbers in Vim, use the following command:

```bash
:set number 
```
or
```bash
:se nu
```

### 1.7. Copy, Cut, Paste, Undo, and Redo in Vim 📋✂️📄

- **Copy Line in Vim:** To copy the current line in Vim, use `yy` in Normal mode.

- **Copy Particular/Multiple Lines in Vim:** To copy specific lines, use `:line_number1,line_number2y` in Normal mode.

- **Paste Above in Vim:** To paste text above the current line, use `P` in Normal mode.

- **Paste Below in Vim:** To paste text below the current line, use `p` in Normal mode.

- **Cut in Vim:** To cut the current line, use `dd` in Normal mode.

- **Delete in Vim:** To delete the current line, use `dd` in Normal mode.

- **Undo in Vim:** To undo the last change, press `u` in Normal mode.

- **Redo in Vim:** To redo the last undone change, press `Ctrl` + `r` in Normal mode.

### 1.8. Insert Using "o" in Vim 🆕

- To insert a new line below the current line, press `o` in Normal mode.

- To insert a new line above the current line, press `O` in Normal mode.

### 1.9. Export Vim as Default Editor 🌟

To set Vim as your default editor, you can export it as the `EDITOR` environment variable. This will make Vim the default editor for various command-line operations that require text input.

```bash
export EDITOR=vim
```

## 2. Learn Nano 🖊️

### 2.1. Open a File in Nano 📂

To open a file in Nano, simply type `nano` followed by the filename.

```bash
$ nano filename
```

- **Example:** Open a file named "example.txt" in Nano.

  ```bash
  $ nano example.txt
  ```

### 2.2. Finding a String in Nano 🔍

Nano provides a basic search functionality by pressing `Ctrl` + `W` and then typing the string you want to find. Press `Ctrl` + `W` again to find the next occurrence.

- **Example:** Search for the word "search" in the file.

  ```bash
  Ctrl + W
  search
  ```

### 2.3. Adding or Modifying Text in Nano ✏️

Nano is straightforward; you can directly start typing to edit the file. There's no need to switch modes.

- **Example:** Add or modify text and save changes in Nano.

  ```bash
  This is some new text.
  Press Ctrl + O to save changes.
  Press Enter to confirm the filename.
  ```

### 2.4. Saving or Closing Files in Nano 💾🚪

To save changes in Nano, press `Ctrl` + `O`, then confirm the filename. To exit Nano, press `Ctrl` + `X`.

- **Example:** Save changes and exit Nano.

  ```bash
  Ctrl + O
  Press Enter to confirm the filename.
  Ctrl + X
  ```

These commands and techniques should help you get started with basic file editing using Vim and Nano. Both editors have their strengths and are widely used in the Unix/Linux command-line environment. Practice is key to becoming proficient with them. Happy editing! 😊👍
