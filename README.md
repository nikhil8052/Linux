 
# Linux File System.

![alt text](https://github.com/nikhil8052/Linux/blob/master/images/filesystem.png?raw=true)

- /boot :- Contains all the files which are required for boot loader.
- /root :- Root User directory.it is not same as /.
- /dev :- System devices such as speakers,printers are configured in this directory.Whenever new device 
          is attached to the Linux System that is noted down in this directory.
- /etc :- All the configuration files of the system on system level such as dns,ntp etc.
- /bin -> usr/bin :- Everyday user commands. 
- /opt  :- Optinal add on application not the system level applications but third-party applications.
- /proc :- Running Process (Curruntly In the Memory).
- /lib :- C programming library files which are required for running commands and apps.
        Check Which library is used for which command.
        strace -e open <command-name>
- /tem :- For temporary Files. 
- /home :- Directory for the User.
- /var :- All the system logs. 
- /mnt :- To mount external File System (NFS).
- /media :- For the CDROM.

# Root 

- Linux has 3 roots.

    Root user account which is most powerfull and can be used to delete,add,modify system confing files
    and other users.

    / the very first directory in the Linux also refered as the root directory.

    The root user account has one root home directory which is refered to root home directory.



# Directory Listing Attributes.

![alt text](https://github.com/nikhil8052/Linux/blob/master/images/file_attributes.png?raw=true)

# Permissions 

![alt text](https://github.com/nikhil8052/Linux/blob/master/images/file_permissions.png?raw=true)


# Login as root.

    sudo su - 

# Connect to putty.

    Find IP address.
    Using ipconfig.
        Troubleshooting 
            If not Found ? First install the net-tools package.
            using apt install net-tools.
            And again fire ifconfig.
            Still not found. 
            Make the interface up. 
            Using ifup interface-name 
                for ubuntu :- ifconfig <interface-name> up 
            Restart your virtual machine. 
            Now,fire ifconfig. 
            You will be good to go now.


