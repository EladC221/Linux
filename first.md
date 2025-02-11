
# 📌 Common Bash Commands

A comprehensive list of **Bash commands**, including file management, process handling, networking, scripting, and DevOps-related tasks. Each command includes an explanation as a comment.

---

## 📁 File System and Directory Management

```bash
# Print the current working directory
pwd

# List files and directories
ls 

# Show detailed information (long format)
ls -l  

# Show hidden files
ls -a  

# Display file sizes in a human-readable format
ls -lh  

# Change to a specific directory
cd /path/to/directory  

# Move up one directory level
cd ..  

# Create a new directory
mkdir folder_name  

# Remove an empty directory
rmdir folder_name  

# Delete a file
rm file_name  

# Delete a directory and its contents
rm -r folder_name  

# Copy a file
cp source destination  

# Copy a directory
cp -r source destination  

# Move or rename a file
mv source destination  

# Create a new empty file
touch file_name  

# Display the contents of a file
cat file_name  

# View file contents with scrolling
more file_name  
less file_name  

# Show the first X lines of a file
head -n X file_name  

# Show the last X lines of a file
tail -n X file_name  

# Continuously monitor a file for changes
tail -f file_name  

🔑 Permissions and Ownership

# Change file permissions
chmod mode file_name  

# Give full read/write/execute permissions
chmod 777 file_name  

# Make a file executable
chmod +x script.sh  

# Change file ownership
chown user:group file_name  

# Search for a file by name
find /path -name "file_name"  

# Quickly find a file (requires updatedb)
locate file_name  

🖥️ Process Management

# List running processes
ps  

# Show all system processes
ps aux  

# Monitor system resource usage
top  

# Interactive process viewer (requires installation)
htop  

# Terminate a process by its ID
kill PID  

# Forcefully kill a process
kill -9 PID  

# Kill processes by name
pkill process_name  

# Show background processes
jobs  

# Bring a background process to the foreground
fg %job_id  

# Resume a background process
bg %job_id  

🌍 Networking and Connectivity

# Test network connectivity to a server
ping domain.com  

# Fetch content from a URL
curl URL  

# Download a file from a URL
wget URL  

# Securely copy a file from a remote server
scp user@server:/path/to/file /local/path  

# Connect to a remote server via SSH
ssh user@server  

# Show open network ports
netstat -tulnp  

# Display network interfaces
ip a  

# Trace the route to a host
traceroute domain.com  

🔁 Loops in Bash

For Loop

# Loop from 1 to 5 and print each number
for i in {1..5}; do
    echo "Number: $i"
done

While Loop

# Loop while a condition is true
count=1
while [ $count -le 5 ]; do
    echo "Counting: $count"
    ((count++))
done

Until Loop

# Run until the condition is met
count=1
until [ $count -gt 5 ]; do
    echo "Still counting: $count"
    ((count++))
done

🔧 Functions in Bash

Basic Function

# Define a simple function
function say_hello() {
    echo "Hello, World!"
}

# Call the function
say_hello

Function with Parameters

# Function with parameters
function greet() {
    echo "Hello $1, how are you today?"
}

# Call the function with an argument
greet "John"

Function with Return Value

# Function that adds two numbers and returns the result
function add_numbers() {
    result=$(( $1 + $2 ))
    echo $result
}

# Store the function result in a variable
sum=$(add_numbers 5 3)
echo "The sum is: $sum"

📜 Bash Scripting

Basic Script

#!/bin/bash
# Simple script that prints a message
echo "This script is running!"

Script with Conditions

#!/bin/bash
# Ask the user for a number and check its value
echo "Enter a number:"
read num

if [ $num -gt 10 ]; then
    echo "The number is greater than 10"
else
    echo "The number is 10 or less"
fi

Script with Loop and Function

#!/bin/bash
# Function that prints numbers from 1 to 5

function print_numbers() {
    for i in {1..5}; do
        echo "Number: $i"
    done
}

# Call the function
print_numbers

🚀 DevOps Commands

🛠️ System Monitoring

# Show system uptime
uptime  

# Show memory usage
free -m  

# Display system performance stats
vmstat  

# Show disk performance stats
iostat  

# Display system activity report
sar  

# Re-run a command every second
watch -n 1 command  

📂 File Archiving & Syncing

# Create a compressed archive
tar -cvzf backup.tar.gz /path/to/dir  

# Sync files between local and remote
rsync -avz /source/ user@server:/destination/  

🐳 Docker Commands

# Show running containers
docker ps  

# List downloaded images
docker images  

# Run a container in detached mode
docker run -d -p 8080:80 image_name  

# Stop a running container
docker stop container_id  

# View real-time logs of a container
docker logs -f container_id  

# Access a running container's shell
docker exec -it container_id bash  

☸️ Kubernetes Commands

# List all running pods
kubectl get pods  

# View logs of a specific pod
kubectl logs pod_name  

# Deploy a Kubernetes configuration file
kubectl apply -f file.yaml  

🛠️ CI/CD (Git, Jenkins, Ansible)

# Clone a repository
git clone repo_url  

# Pull the latest changes
git pull  

# Commit changes
git commit -m "message"  

# Push changes to the repository
git push origin branch_name  

# Run an Ansible playbook
ansible-playbook playbook.yml  

🏆 Bonus: Useful Bash Shortcuts

# Stop a running command
Ctrl + C  

# Suspend a process
Ctrl + Z  

# Exit the terminal
Ctrl + D  

# Repeat the last command
!!  

This Markdown file ensures proper syntax highlighting, clear readability, and detailed comments for every command. You can directly upload this to GitHub or any other platform that supports Markdown formatting. 🚀