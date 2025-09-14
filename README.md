# linux-for-devops

# 📂 Linux Commands Cheatsheet

---

## ✅ Basic Navigation Commands

| Command | Description | Flags / Notes | Example |
|------|--------------|----------------|--------|
| `cd` | Change directory | No flags | `cd /home/user` |
| `cd ..` | Move to the parent directory | No flags | `cd ..` |
| `pwd` | Print the current working directory | No flags | `pwd` |

---

## ✅ Listing Files and Directories

| Command | Description | Flags / Notes | Example |
|------|--------------|----------------|--------|
| `ls` | List files and directories | No flags by default | `ls` |
| `ls -l` | List files with detailed information (permissions, owner, size, etc.) | `-l` for long listing format | `ls -l` |

---

## ✅ Directory Creation and Removal

| Command | Description | Flags / Notes | Example |
|------|--------------|----------------|--------|
| `mkdir` | Create new directory | No flags | `mkdir new_folder` |
| `rmdir` | Remove empty directory | No flags | `rmdir old_folder` |
| `rm` | Remove files | No flags by default | `rm file.txt` |
| `rm -r` | Recursively remove directories and contents | `-r` for recursive deletion | `rm -r old_folder` |

---

## ✅ File Manipulation

| Command | Description | Flags / Notes | Example |
|------|--------------|----------------|--------|
| `touch` | Create an empty file or update timestamp | No flags | `touch newfile.txt` |
| `cat` | Concatenate and display file content | No flags by default | `cat file.txt` |
| `echo "something" > file.txt` | Write text into a file (overwrites existing content) | `>` redirects output | `echo "Hello World" > file.txt` |
| `head` | Show first lines of a file | Default shows first 10 lines | `head file.txt` |
| `tail` | Show last lines of a file | Default shows last 10 lines | `tail file.txt` |
| `tail -f` | Continuously output appended data (useful for logs) | `-f` follow the file | `tail -f logfile.log` |
| **Exit `tail -f`** | Stop following | Press `Ctrl + C` | — |

---

## ✅ Viewing File Content

| Command | Description | Flags / Notes | Example |
|------|--------------|----------------|--------|
| `less` | View file one page at a time; scrollable | Navigate with arrow keys | `less file.txt` |
| `more` | Similar to less but simpler; view one page at a time | Navigate with space or Enter | `more file.txt` |

---

