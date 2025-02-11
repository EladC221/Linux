# 📌 Common Bash Commands

A structured list of **Bash commands** with their explanations, available options, and example usage.

---

## **pwd** - Print the current working directory
```bash
pwd  # Prints the absolute path of the current directory
```

---

## **ls** - List files and directories
```bash
ls  # Lists files and directories in the current directory
```
### **Options:**
```bash
ls -l    # Detailed list (long format)
ls -a    # Show hidden files
ls -lh   # Human-readable file sizes
ls -lt   # Sort by modification time
```

---

## **cd** - Change directory
```bash
cd /path/to/directory  # Navigate to a specific directory
cd ..  # Move up one directory level
```

---

## **mkdir** - Create a new directory
```bash
mkdir folder_name  # Create a directory named "folder_name"
```

---

## **rmdir** - Remove an empty directory
```bash
rmdir folder_name  # Deletes an empty directory
```

---

## **rm** - Remove files or directories
```bash
rm file_name  # Deletes a file
rm -r folder_name  # Deletes a directory and its contents
```

---

## **cp** - Copy files and directories
```bash
cp source destination  # Copy a file
cp -r folder1 folder2  # Copy a directory recursively
```

---

## **mv** - Move or rename files and directories
```bash
mv old_name new_name  # Rename a file or folder
mv file.txt /new/path/  # Move file to a new location
```

---

## **touch** - Create a new empty file
```bash
touch new_file.txt  # Creates an empty file
```

---

## **cat** - Display file contents
```bash
cat file_name  # Display file content in the terminal
```

---

## **tail** - Display the last lines of a file
```bash
tail -n 10 file_name  # Show the last 10 lines
```
### **Options:**
```bash
tail -f file_name  # Monitor a file for live updates
```

---

## **chmod** - Change file permissions
```bash
chmod +x script.sh  # Make a script executable
chmod 777 file.txt  # Give full read/write/execute permissions to everyone
```

---

## **chown** - Change file owner and group
```bash
chown user:group file.txt  # Change owner of a file
```

---

## **find** - Search for files
```bash
find /path -name "file.txt"  # Find a file by name
```
### **Advanced Usage:**
```bash
find /var/logs -name "*.log" -mtime -7  # Find all .log files modified in the last 7 days
```

---

## **grep** - Search for patterns in files
```bash
grep "search_term" file.txt  # Find occurrences of a term in a file
```
### **Options:**
```bash
grep -i "search_term" file.txt  # Case insensitive search
grep -r "search_term" /directory/  # Recursive search in directories
```

---

## **User Management and Permissions**
```bash
# Create a new user
sudo useradd -m new_user

# Change user password
passwd new_user

# Add user to sudo group
sudo usermod -aG sudo new_user
```

---

## **Bonus: Useful Bash Shortcuts**
| **Shortcut** | **Description** |
|-------------|---------------|
| `Ctrl + C` | Stop a running command |
| `Ctrl + Z` | Suspend a process |
| `Ctrl + D` | Exit the terminal |
| `Ctrl + R` | Reverse search through history |
| `Alt + .` | Insert last argument of previous command |
| `!!` | Run the last command again |

---

## **Advanced Bash Scripting Tips**
```bash
#!/bin/bash
trap "echo 'You pressed Ctrl+C! Exiting...'; exit 1" SIGINT

for i in {1..5}; do
    echo "Looping: $i"
    sleep 1
done
```

---
