# Linux (Ubuntu) Commands Cheat Sheet

## 1. Basic Commands

### File & Directory Operations

| **Command** | **Description** | **Example** |
|--------------|----------------|--------------|
| `pwd` | Print current working directory (shows where you are). | `pwd` |
| `ls` | List files and directories. | `ls -l` |
| `cd` | Change directory. | `cd /home/user/Documents` |
| `mkdir` | Create a new directory. | `mkdir new_project` |
| `rmdir` | Remove an empty directory. | `rmdir old_folder` |
| `rm` | Remove files or directories. | `rm file.txt` or `rm -r folder` |
| `cp` | Copy files or directories. | `cp file.txt backup/` |
| `mv` | Move or rename files/directories. | `mv old.txt new.txt` |

---

### File Viewing & Editing

| **Command** | **Description** | **Example** |
|--------------|----------------|--------------|
| `cat` | Display file content in terminal. | `cat notes.txt` |
| `less` | View large text files page by page. | `less logfile.txt` |
| `touch` | Create an empty file or update timestamp. | `touch newfile.txt` |
| `echo` | Print text or variables to terminal. | `echo "Hello, world!"` |
| `nano` | Simple text editor in terminal. | `nano script.sh` |
| `vim` | Advanced terminal-based text editor. | `vim config.txt` |

---

### System & Package Management

| **Command** | **Description** | **Example** |
|--------------|----------------|--------------|
| `sudo` | Run a command with superuser privileges. | `sudo apt update` |
| `apt` | Install, update, or remove packages (Debian/Ubuntu). | `sudo apt install vim` |
| `df` | Show disk space usage of mounted filesystems. | `df -h` |
| `du` | Show disk usage of files/folders. | `du -sh *` |

---

### Process & System Monitoring

| **Command** | **Description** | **Example** |
|--------------|----------------|--------------|
| `ps` | Display running processes. | `ps aux` |
| `top` | Show system resource usage in real-time. | `top` |
| `htop` | Interactive process viewer (requires install). | `sudo apt install htop && htop` |

---

### Searching

| **Command** | **Description** | **Example** |
|--------------|----------------|--------------|
| `grep` | Search for text in files. | `grep "main" *.cpp` |

---

## 2. Intermediate Commands

### Archiving & Compression

| **Command** | **Description** | **Example** |
|--------------|----------------|--------------|
| `tar` | Create or extract compressed archives. | `tar -czvf backup.tar.gz folder/` |
| `gzip` / `gunzip` | Compress or decompress files. | `gzip data.txt` |
| `zip` / `unzip` | Create or extract ZIP files. | `zip -r project.zip folder/` |

---

### Permissions & Ownership

| **Command** | **Description** | **Example** |
|--------------|----------------|--------------|
| `chmod` | Change file permissions. | `chmod 755 script.sh` |
| `chown` | Change file ownership. | `sudo chown user:group file.txt` |
| `whoami` | Show current logged-in user. | `whoami` |
| `id` | Show user and group IDs. | `id` |

---

### Networking

| **Command** | **Description** | **Example** |
|--------------|----------------|--------------|
| `ping` | Test network connectivity. | `ping google.com` |
| `curl` | Fetch data from URLs or APIs. | `curl https://example.com` |
| `wget` | Download files from the internet. | `wget https://example.com/file.zip` |
| `ip a` | Show network interfaces and IP addresses. | `ip a` |
| `ssh` | Connect to another machine securely. | `ssh user@192.168.1.10` |
| `scp` | Securely copy files between systems. | `scp file.txt user@host:/path/` |

---

### System Info & Hardware

| **Command** | **Description** | **Example** |
|--------------|----------------|--------------|
| `uname -a` | Show system kernel and architecture info. | `uname -a` |
| `lscpu` | Display CPU information. | `lscpu` |
| `lsblk` | List block devices (disks and partitions). | `lsblk` |
| `free -h` | Show memory usage. | `free -h` |
| `uptime` | Show how long the system has been running. | `uptime` |
| `dmesg | tail` | View recent kernel/system messages. | `dmesg | tail` |

---

### File Searching & Management

| **Command** | **Description** | **Example** |
|--------------|----------------|--------------|
| `find` | Search for files or directories. | `find /home -name "*.cpp"` |
| `locate` | Quickly find files using an index (use `sudo updatedb` first). | `locate config.json` |
| `head` | Display first lines of a file. | `head -n 10 file.txt` |
| `tail` | Display last lines of a file (useful for logs). | `tail -f /var/log/syslog` |

---

### Logs & Systemd

| **Command** | **Description** | **Example** |
|--------------|----------------|--------------|
| `journalctl` | View logs from systemd. | `journalctl -xe` |
| `systemctl` | Control and inspect system services. | `sudo systemctl status nginx` |
| `service` | Start or stop system services. | `sudo service ssh restart` |

---

### Chain commands:  
  ```bash
  mkdir new && cd new && touch readme.md
