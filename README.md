 
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



# How to change password. 

    passwd username (cammand)

    It will fisrt ask for your old password and then you need to enter your new password.

# Wild Card in Linux.

    Wild Card :- Wild card is nothing but a character which is used to represent one or more character.It is used for searches,creating multiple files, deleting multiple files etc.Linux provides many wild cards
    to work with. 

    * :- Represent the one or more characters. 
    ? :- Represents the Single Character.
    [] :- Represents the range of characters.
    !  :- Excludes characters inside the brackets.

    Examples 

    - Find files which has a in the beginning and end in the end and middle character can be 
    anything and the length of the string must be three. 

    ls -l a?c
    
    - create 100 files which must be named as user1,user2,user3 and so on .

    touch user[1..100]

    - Search file which has ab in the beginning.

    ls -l ab*

    - finds bill and bull, but not ball or bell

    b[!ae]ll




