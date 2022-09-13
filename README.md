 
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


# Soft Links Vs Hard Links 

- Links :- Links are nothing but the shortcuts of accessing files.Links are used to refer the same file with multiple names.

Note:- Soft link can be created for files and directories but hard link can only be created for files only not for directories. 

- inode :- It's a number or a pointer to a file on the hard disk.

 ls -i abc  (command to find the inode number of any file )
 ls -di abc  (command to find the inode number of any directory )
 find / -inum inode_number(Find all the locations )

- Hard Link 

    If the orignal file is deleted from the destination. We can access the same content using the 
    Hard Link.

    Links have actual file contents.

    The size of any of the hard link file is same as the original file and if we change the content in any of the hard links then size of all hard link files are updated.

    In hard link inode number remains the same as the orignal one.

    Data reflects in the hard link if we change the hard linked refering file content it will automatically 
    will be updated on the other locations as the inode number is same in this case.

    Size remains same in the hard link.

    Hard link cannot be created across the partitions.

    ln  [original filename] [link name] 

- Soft Link 

    Link will be removed if the file is removed.

    A soft link is similar to the file shortcut feature which is used in Windows Operating systems

    Soft Link contains the path for original file and not the contents.

    Removing soft link doesn’t affect anything but removing original file, the link becomes “dangling” link which points to nonexistent file.

    A soft link can link to a directory.

    The size of the soft link is equal to the length of the path of the original file 

    If we change the name of the original file then all the soft links for that file become dangling i.e. they are worthless now.

    ln  -s [original filename] [link name] 


# Check OS version 

    - cat /etc/system-release


# Command Syntax

- command -options -arguments 

- Command contains option and arguments.

- Options :- It modify the way of working of a command. It usually contains a hyphen or dash symbal followed
 by a single character.Some commands contains multiple options which can be grouped together after the hyphen.

- Arguments :- Some command assumne default argument if non is supplied.Arguments are optinal for some commands and required for some .

- Example :- 

   ls -ltr (ltr are the options to the command which specify listing out the things in decending order of time.)

   ls -l test (here file name test is an argument to the listing command )

   rm -f test (Remove the file forcefully) 

   rm -r (To remove a directory)

# Get info about the command 

- man ls (Gives the manual of ls command.)

# Files and Directory Permissions 

- Unix is a multi-user system. Every user has files and directory own by him/her.Every file and directory can be protected to to make accessibe to other users by changing the file permissions.

- There are three types of permissions.
    -r read 
    -x execute or running a program 
    -w write 

- Each permission can be controlled at three levels .

    user - Yourself.   (u)
    group - can be people in the same project. (g)
    other - Everyone   (o)

Permissions can be shown by ls -l command 

![alt text](https://github.com/nikhil8052/Linux/blob/master/images/file_users_mode.png?raw=true)

# command to change permissions of a file and directory 

- chmod 

- Example 

    chmod g -w test (Remove the write  permission from the group.)

    chmod a-r (Remove read permission from all (User,Group,Others))

    chmod u+rw (Give the read and write permission)

    chmod g+rw (Give the read and write permission to group)
