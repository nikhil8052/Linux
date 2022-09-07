# How to find IP Address of machine first time. 

Use command 
 
    ip addr
    ip 

Make sure that you have downloaded the package net-tools before using this command. 

    yum install net-tools


# Assign IP to the Linux machine (VM)

    Step 1 :- Go to the Virtual Box.
    Step 2 :- Settings.
    Step 3 :- Network.
    Step 4 :- Change Adapter to host only adapter.

    And then fire ifconfig command. 

    if still you are not able to find IP.

    Then login as root user.

    Make the interface up or active using. (ifup name-of-interface )
        UBUNTU:- ifconfig <interface> up.

    ifup :- ifup activates a network interface, making it available to transmit and receive data.

    And again try then you will be finding your IP. 

# Host Only Adapter.

    Allow communication between the PC and the virtual Machine.

# Bridge Adapter.

    Allow communication between the PC and VM plus allow communication to the internet.

# Activate the interface.

    ifup activates a network interface, making it available to transmit and receive data.