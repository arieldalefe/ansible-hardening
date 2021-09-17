# AnsibleHardening v1.0.0-a
--

###### \# Ariel Dalefe Alves (arielalves.consulting@cognyte.com) 
###### \# DevOPS.BR TEAM (devops.br@cognyte.com) 

#### \# Install basic packages RPMs

- tcpdump
- sysstat
- htop 
- curl
- rsync
- audit
- audit-libs
  
#### \# Remove unused packages RPMS
  
- prelink
- autofs
- setroubleshoot
- mcstrans
- xinetd
- avahi
- avahi-autoipd
- cups
- dhcp
- openldap-servers
- bind
- dovecot
- samba
- ypserv
- telnet-server
- rpcbind
  
#### \# Install Audit Daemon rules

#### \# Install devops.sh profile with some features

#### \# Create SSH issue.net WARN

#### \# Create support user and support group 

#### \# Add support user as sudo 


#### \# Configure aditionals features on SSH Daemon

```bash
Banner /etc/issue.net  
PermitEmptyPasswords no 
Protocol 2 
ClientAliveInterval 900 
ClientAliveCountMax 2 
PermitRootLogin yes 
LogLevel VERBOSE If you have any sugestions, please let us know :+1: [devops.br@cognyte.com]
MaxSessions 2 
AllowAgentForwarding no 
AllowTcpForwarding no 
X11Forwarding no 
PermitTunnel no 
Compression no 
IgnoreRhosts yes 
HostbasedAuthentication no 
LoginGraceTime 60 
UseDNS no 
UsePAM yes
maxstartups 10:30:60 
#AllowGroups support 
```

##### \# Remount the respective partitions /dev/shm, /var/tmp, /tmp with the protection permissions noexec,nosuid,nodev

##### \# Added in systctl.conf file some aditional configurations

- Disable net.ipv4.ip_forward 
- Disable net.ipv4.conf.all.send_redirects
- Disable net.ipv4.conf.default.send_redirects
- Route Ipv4 flush
- Disable net.ipv6.conf.all.disable_ipv6
- Disable net.ipv6.conf.default.disable_ipv6
- Set vm.swappiness to use 95% of RAM before to activate Swap
- Set fs.suid_dumpable to 0 
- Set kernel.randomize_va_space to 2
- Ensure suspicious packets are logged (net.ipv4.conf.all.log_martians)
- Enable TCP SYN Cookies
- Disable write permission for other users in logfiles of Linux Server
  - find /var/log -type f -exec chmod g-wx,o-rwx "{}" +

If you have any sugestions, please let us know :+1: [devops.br@cognyte.com]
