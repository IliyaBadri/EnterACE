# Basic Linux Commands Documentation

This documentation provides an overview of the basic Linux commands frequently used in a terminal or shell environment. Familiarity with these commands is essential for navigating and managing files and directories, executing programs, and performing various administrative tasks on a Linux system.

Please note that this documentation assumes a basic understanding of the Linux operating system and a working terminal or shell environment.

## Table of Contents

1. [Navigating the File System](#navigating-the-file-system)
   - `cd`
   - `ls`
   - `pwd`
   
2. [Working with Files and Directories](#working-with-files-and-directories)
   - `mkdir`
   - `touch`
   - `cp`
   - `mv`
   - `rm`
   
3. [Viewing and Editing Files](#viewing-and-editing-files)
   - `cat`
   - `less`
   - `head`
   - `tail`
   - `nano`
   - `vim`
   
4. [File Permissions and Ownership](#file-permissions-and-ownership)
   - `chmod`
   - `chown`
   
5. [Working with Processes](#working-with-processes)
   - `ps`
   - `top`
   - `kill`
   
6. [Managing Users and Groups](#managing-users-and-groups)
   - `adduser`
   - `passwd`
   - `usermod`
   - `groupadd`
   - `groupmod`
   
7. [Networking](#networking)
   - `ping`
   - `ifconfig`
   - `ssh`
   
8. [System Information](#system-information)
   - `uname`
   - `lsb_release`
   - `df`
   - `du`

## Navigating the File System

### `cd`

Change the current directory.

```bash
cd [directory]
```

- `cd` - Change to the home directory.
- `cd /path/to/directory` - Change to the specified directory.
- `cd ..` - Move up to the parent directory.
- `cd -` - Switch to the previous directory.

### `ls`

List files and directories in the current directory.

```bash
ls [options] [directory]
```

- `ls` - List files and directories in the current directory.
- `ls -l` - List files and directories in long format.
- `ls -a` - List all files and directories, including hidden ones.
- `ls -lh` - List files and directories in long format with human-readable sizes.

### `pwd`

Print the current working directory.

```bash
pwd
```

## Working with Files and Directories

### `mkdir`

Create a new directory.

```bash
mkdir [directory]
```

- `mkdir directory` - Create a directory with the specified name.
- `mkdir -p directory/subdirectory` - Create parent directories if they don't exist.

### `touch`

Create an empty file or update the timestamp of an existing file.

```bash
touch [file]
```

- `touch file` - Create a new file with the specified name.
- `touch -r existingfile newfile` - Update the timestamp of `newfile` to match `existingfile`.

### `cp`

Copy files and directories.

```bash
cp [options] source destination
```

- `cp file destination` - Copy a file to the specified destination.
- `cp -r directory destination` - Copy a directory and its contents recursively.
- `cp -a source destination` - Preserve file attributes while copying.

### `mv`

Move or rename files and directories.

```bash
mv [options] source destination
```



- `mv file destination` - Move or rename a file to the specified destination.
- `mv directory newname` - Rename a directory.
- `mv file1 file2 directory` - Move multiple files to a directory.

### `rm`

Remove files and directories.

```bash
rm [options] file
```

- `rm file` - Remove a file.
- `rm -r directory` - Remove a directory and its contents recursively.
- `rm -f file` - Forcefully remove a file without prompting.

## Viewing and Editing Files

### `cat`

Concatenate and display the contents of files.

```bash
cat [file]
```

- `cat file` - Display the contents of a file.
- `cat file1 file2` - Display the contents of multiple files concatenated.

### `less`

View files interactively.

```bash
less [file]
```

- `less file` - View the contents of a file interactively.
- Use the arrow keys to scroll up and down. Press `q` to exit.

### `head`

Display the beginning of a file.

```bash
head [options] [file]
```

- `head file` - Display the first 10 lines of a file.
- `head -n 5 file` - Display the first 5 lines of a file.
- `head -c 100 file` - Display the first 100 bytes of a file.

### `tail`

Display the end of a file.

```bash
tail [options] [file]
```

- `tail file` - Display the last 10 lines of a file.
- `tail -n 5 file` - Display the last 5 lines of a file.
- `tail -f file` - Continuously display the last lines of a file as it grows (useful for log files).

### `nano`

A simple command-line text editor.

```bash
nano [file]
```

- `nano file` - Open the specified file in the nano text editor.
- Use the displayed commands at the bottom to navigate and edit the file.
- Press `Ctrl + X` to exit nano.

### `vim`

A powerful command-line text editor.

```bash
vim [file]
```

- `vim file` - Open the specified file in the vim text editor.
- Press `i` to enter insert mode and start editing.
- Press `Esc` to exit insert mode.
- Use `:wq` to save and exit, or `:q!` to exit without saving.

## File Permissions and Ownership

### `chmod`

Change the permissions of files and directories.

```bash
chmod [options] mode file
```

- `chmod u+x file` - Add execute permission for the owner.
- `chmod go-rwx file` - Remove read, write, and execute permissions for the group and others.
- `chmod 755 file` - Set read, write, and execute permissions for the owner, and read and execute permissions for the group and others.

### `chown`

Change the ownership of files and directories.

```bash
chown [options] user:group file
```

- `chown user:group file` - Change the owner and group of a file.

## Working with Processes

### `ps`

List active processes.

```bash
ps [options]
```

- `ps` - List the currently running processes.
- `ps aux` - List all processes with detailed information.
- `ps -ef` - List all processes in full format.

### `top`

Monitor system processes in real-time.

```bash
top
```

- `top` - Display a live view of system resource usage.
- Press `q

` to exit top.

### `kill`

Terminate a process.

```bash
kill [options] process_id
```

- `kill process_id` - Terminate a process with the specified process ID.
- `killall process_name` - Terminate all processes with the specified name.

## Managing Users and Groups

### `adduser`

Create a new user.

```bash
adduser [username]
```

- `adduser username` - Create a new user with the specified username.
- Follow the prompts to set the password and other user details.

### `passwd`

Change a user's password.

```bash
passwd [username]
```

- `passwd username` - Change the password for the specified user.
- Follow the prompts to enter the new password.

### `usermod`

Modify user account settings.

```bash
usermod [options] username
```

- `usermod -aG groupname username` - Add a user to a group.
- `usermod -l newusername username` - Rename a user.

### `groupadd`

Create a new group.

```bash
groupadd [groupname]
```

- `groupadd groupname` - Create a new group with the specified name.

### `groupmod`

Modify group settings.

```bash
groupmod [options] groupname
```

- `groupmod -n newgroupname groupname` - Rename a group.

## Networking

### `ping`

Check network connectivity.

```bash
ping [host]
```

- `ping host` - Send ICMP echo requests to a host to check if it's reachable.
- Press `Ctrl + C` to stop pinging.

### `ifconfig`

Display network interface information.

```bash
ifconfig [interface]
```

- `ifconfig` - Display information for all network interfaces.
- `ifconfig interface` - Display information for a specific network interface.

### `ssh`

Securely access remote machines.

```bash
ssh [user@]host [command]
```

- `ssh user@host` - Connect to a remote host as a specific user.
- `ssh user@host command` - Run a command on a remote host.

## System Information

### `uname`

Display system information.

```bash
uname [options]
```

- `uname` - Display the system's kernel name, node name, kernel release, kernel version, machine hardware name, and processor type.
- `uname -a` - Display all available system information.

### `lsb_release`

Display Linux Standard Base (LSB) information.

```bash
lsb_release [options]
```

- `lsb_release -a` - Display LSB information about the Linux distribution.

### `df`

Display disk space usage.

```bash
df [options] [directory]
```

- `df` - Display disk space usage for all mounted filesystems.
- `df -h` - Display disk space usage in human-readable format.
- `df directory` - Display disk space usage for the specified directory.

### `du`

Estimate file and directory space usage.

```bash
du [options] [directory]
```

- `du` - Estimate space usage for the current directory and its subdirectories.
- `du -h` - Estimate space usage in human-readable format.
- `du -s directory` - Estimate space usage for the specified directory.

This concludes the basic Linux commands documentation. These commands provide a solid foundation for working with Linux systems and managing files, processes, users, and network connections. Experimenting and exploring further will enhance your understanding and proficiency in Linux command-line operations.
