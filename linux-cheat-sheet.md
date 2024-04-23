1. **Manage System Services with systemd:**

   - Start a service:
   ```bash
   sudo systemctl start service_name

Stop a service:
```
sudo systemctl stop service_name
```
Restart a service:
```
sudo systemctl restart service_name
```

2. **Manage Firewall Rules with UFW:**

Enable UFW (Uncomplicated Firewall):
```
sudo ufw enable
```

Allow incoming traffic for a specific port:
```
sudo ufw allow port_number
```

Deny incoming traffic for a specific port:
```
sudo ufw deny port_number
```

3. **Manage Users and Groups:**
Create a new user:
```
sudo adduser username
```

Add a user to a group:
```
sudo usermod -aG groupname username
```

Change user password:
```
sudo passwd username
```

4. **View System Logs:**

View system messages:
```
dmesg
```

View system log:
```
tail -f /var/log/syslog
```

5. **Monitor System Resources:**

Check memory usage:
```
free -h
```

Check CPU usage:
```
top
```

6. **Manage Disk Partitions:**
List disk partitions:
```
sudo fdisk -l
```

Format a disk partition:
```
sudo mkfs.ext4 /dev/sdX1
```

Mount a disk partition:
```
sudo mount /dev/sdX1 /mnt
```

7. **Manage Software Repositories:**
Add a new repository:
```
sudo add-apt-repository repository_url
```

Remove a repository:
```
sudo add-apt-repository --remove repository_url
```
8. **Check Network Configuration:**
Display network interfaces:
```
ip addr show
```

Check network connectivity:
```
ping domain.com
```

9. **Manage SSH Connections:**
```
Allow SSH connections:
```

Disable SSH root login:

Edit /etc/ssh/sshd_config and set PermitRootLogin no, then restart SSH service.

10. **Install Software from Source:**

Extract source tarball:
```
tar -zxvf source.tar.gz
```
Navigate to the extracted directory and follow the installation instructions provided in the README or INSTALL file.






4. 

