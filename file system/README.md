# Navigation to File System. 

- cd :- Change Directory. 
- pwd :- Print Current Working Directory.
- ls :- List all the folders and files of a directory.
- ls -l :- Long Listing.


# Directory Listing Attributes.

![alt text](https://github.com/nikhil8052/Linux/blob/master/images/file_attributes.png?raw=true)

# Permissions 

![alt text](https://github.com/nikhil8052/Linux/blob/master/images/file_permissions.png?raw=true)

# File Types.

![alt text](https://github.com/nikhil8052/Linux/blob/master/images/file_types.png?raw=true)


# Create new file. 

touch <filename> <filename>

It creates the empty file. 

# Copy the one file to other. 

cp <source-file> <distination-file>

# Copy the Folders. 

cp -R  <source-folder> <distination-folder>

Here the -R specify the recusevily copy all the content of the folder to the other folder. 

# Find Files and Directories in Linux.

Using commands :- find,locate

Start search from the root 
    find / -name "test"

Find in the current folder or sub-folders  
    find . -name "test.cpp" 

Find using locate in the current folder 
    locate test.cpp 

    locate command does not return any result so then as a root run --> updatedb.

    Make sure that we have ( mlocate )  package installed.

    To check whether installed or not please fire. 

    rpm -qa | grep mlocate 

    To install the package.

    apt install mlocate.

    
# Locate Vs Find command. 

locate 

    locate command has its own database,which should be regularly updated while find command 
    iterate over the file system to locate or find the file.Thus, the locate command is much
    faster than the find command but can give the inaccurate data if the db is not updated. 
    We can update the db using the updatedb. if we don't do it so after a particular time 
    OS automatically update the DB.

    Database of the locate command can be updated by root only.
    
