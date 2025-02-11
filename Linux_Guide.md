# 📌 Common Bash Commands

A comprehensive list of **Bash commands**, including file management, process handling, networking, scripting, and DevOps-related tasks. Each command includes an explanation as a comment.

---

## 📁 File System and Directory Management

### **pwd - Print Current Directory**
```bash
pwd  # Prints the absolute path of the current working directory
```

### **ls - List Files and Directories**
```bash
ls  # List all files and directories
ls -l  # Show detailed information (long format)
ls -a  # Show hidden files
ls -lh  # Display file sizes in a human-readable format
```

### **cd - Change Directory**
```bash
cd /path/to/directory  # Change to a specific directory
cd ..  # Move up one directory level
```

### **mkdir & rmdir - Manage Directories**
```bash
mkdir folder_name  # Create a new directory
rmdir folder_name  # Remove an empty directory
```

### **rm - Remove Files & Directories**
```bash
rm file_name  # Delete a file
rm -r folder_name  # Remove a directory and its contents
```

### **cp - Copy Files and Directories**
```bash
cp source destination  # Copy a file
cp -r source destination  # Copy a directory
```

### **mv - Move or Rename Files**
```bash
mv source destination  # Move or rename a file
```

### **touch - Create an Empty File**
```bash
touch file_name  # Create a new empty file
```

### **cat, more, less - View File Contents**
```bash
cat file_name  # Display the contents of a file
more file_name  # View file contents with scrolling
less file_name  # Similar to more, but allows backward scrolling
```

### **head & tail - View Portions of Files**
```bash
head -n X file_name  # Show the first X lines of a file
tail -n X file_name  # Show the last X lines of a file
tail -f file_name  # Continuously monitor a file for changes
```

---

## 🔑 Permissions and Ownership

### **chmod - Change File Permissions**
```bash
chmod mode file_name  # Change file permissions
chmod 777 file_name  # Give full read/write/execute permissions
chmod +x script.sh  # Make a script executable
```

### **chown - Change File Ownership**
```bash
chown user:group file_name  # Change ownership of a file
```

### **find & locate - Search for Files**
```bash
find /path -name "file_name"  # Search for a file by name
locate file_name  # Quickly find a file (requires updatedb)
```

---

## 🖥️ Process Management

### **ps - List Running Processes**
```bash
ps  # Show running processes
ps aux  # Show all system processes
```
## 🖥️ Process Management

### **top - Monitor System Resource Usage**
```bash
top  # Show real-time system performance and resource usage
```

### **htop - Interactive Process Viewer** *(Requires installation)*
```bash
htop  # A more user-friendly process viewer compared to 'top'
```

### **kill & pkill - Terminate Processes**
```bash
kill PID  # Terminate a process by its ID
kill -9 PID  # Forcefully kill a process
pkill process_name  # Kill processes by name
```

### **Background Process Management**
```bash
jobs  # Show background processes
fg %job_id  # Bring a background process to the foreground
bg %job_id  # Resume a background process
```

---

## 🌍 Networking and Connectivity

### **ping - Test Network Connectivity**
```bash
ping domain.com  # Send ICMP packets to check connectivity
```

### **curl & wget - Fetch Data from URLs**
```bash
curl URL  # Fetch content from a URL
wget URL  # Download a file from a URL
```

### **scp - Secure Copy Over SSH**
```bash
scp user@server:/path/to/file /local/path  # Copy a file from a remote server
```

### **ssh - Remote Server Connection**
```bash
ssh user@server  # Connect to a remote server
```

### **Network Utilities**
```bash
netstat -tulnp  # Show open network ports
ip a  # Display network interfaces
traceroute domain.com  # Show the route taken to a host
```

---

## 🔁 Loops in Bash

### **For Loop**
```bash
for i in {1..5}; do
    echo "Number: $i"
done
```

### **While Loop**
```bash
count=1
while [ $count -le 5 ]; do
    echo "Counting: $count"
    ((count++))
done
```

### **Until Loop**
```bash
count=1
until [ $count -gt 5 ]; do
    echo "Still counting: $count"
    ((count++))
done
```

---

## 🔧 Functions in Bash

### **Basic Function**
```bash
function say_hello() {
    echo "Hello, World!"
}
say_hello
```

### **Function with Parameters**
```bash
function greet() {
    echo "Hello $1, how are you today?"
}
greet "John"
```
## 🔧 Functions in Bash

### **Function that Adds Two Numbers**
```bash
function add_numbers() {
    result=$(( $1 + $2 ))
    echo $result
}

# Store the function result in a variable
sum=$(add_numbers 5 3)
echo "The sum is: $sum"
```

---

## 📜 Bash Scripting

### **Basic Script**
```bash
#!/bin/bash
# Simple script that prints a message
echo "This script is running!"
```

### **Script with Conditions**
```bash
#!/bin/bash
# Ask the user for a number and check its value
echo "Enter a number:"
read num

if [ $num -gt 10 ]; then
    echo "The number is greater than 10"
else
    echo "The number is 10 or less"
fi
```

### **Script with Loop and Function**
```bash
#!/bin/bash
# Function that prints numbers from 1 to 5

function print_numbers() {
    for i in {1..5}; do
        echo "Number: $i"
    done
}

# Call the function
print_numbers
```

---

## 🚀 DevOps Commands

### **System Monitoring**
```bash
uptime  # Show system uptime
free -m  # Show memory usage
vmstat  # Display system performance stats
iostat  # Show disk performance stats
sar  # Display system activity report
watch -n 1 command  # Re-run a command every second
```

### **File Archiving & Syncing**
```bash
tar -cvzf backup.tar.gz /path/to/dir  # Create a compressed archive
rsync -avz /source/ user@server:/destination/  # Sync files between local and remote
```

### **Docker Commands**
```bash
docker ps  # Show running containers
docker images  # List downloaded images
docker run -d -p 8080:80 image_name  # Run a container in detached mode
docker stop container_id  # Stop a running container
docker logs -f container_id  # View real-time logs of a container
docker exec -it container_id bash  # Access a running container's shell
```

### **Kubernetes Commands**
```bash
kubectl get pods  # List all running pods
```
## ☸️ Kubernetes Commands

### **View Pod Logs**
```bash
kubectl logs pod_name  # View logs of a specific pod
```

### **Deploy a Configuration File**
```bash
kubectl apply -f file.yaml  # Deploy a Kubernetes configuration file
```

---

## 🛠️ CI/CD (Git, Jenkins, Ansible)

### **Git Commands**
```bash
git clone repo_url  # Clone a repository
git pull  # Pull the latest changes
git commit -m "message"  # Commit changes
git push origin branch_name  # Push changes to the repository
```

### **Ansible Commands**
```bash
ansible-playbook playbook.yml  # Run an Ansible playbook
```

---

## 🏆 Bonus: Useful Bash Shortcuts

| **Shortcut** | **Description** |
|-------------|----------------|
| `Ctrl + C`  | Stop a running command |
| `Ctrl + Z`  | Suspend a process |
| `Ctrl + D`  | Exit the terminal |
| `!!`        | Repeat the last command |

---

