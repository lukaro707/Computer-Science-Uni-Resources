# Command Syntax:
## Description of command and parameters
- Command pre-requisites (mode, device, etc.)
	- command *parameter* 
 	- alternatecommand *parameter*

# Mode Changes
## Enter Privileged Exectuive Mode
- User Exectuive Mode
	- enable
		
## Enter Host Configuration Mode
- Privileged Executive Mode
	- configure terminal
 	- config t

## Return to Privileged Executive Mode
- Any mode higher than Host Configuration Mode
	- end

# Basic configuration
## Change the path of the boot environment variable to *file path*
- Host Configuration Mode
	- boot *file path*

## Set the host name of the device
- Host Configuration Mode
	- hostname *hostname*

## Set an encrypted password on the enable command
- Host Configuration Mode
	- enable secret *password*

## Enter line configuration mode for console 0 (used to set password for device)
- Host Configuration Mode
	- line console 0

## Enter line configuration mode for vty 0-4 (used to set password for... I'm not sure actually)
- Host Configuration mode
	- line vty 0 4

## Set the login password of the current line(s)
- Line Configuration Mode
	- password *password* <br>
 	login

## Encrypt all passwords
- Host Cofiguration Mode
	- service password-encryption

## Set a banner message of the day
- Host Configuration Mode
	- banner motd #*message of the day*#

## Save the current running configuration to the startup configuration
- Privileged Executive Mode
	- copy running-config startup-config : copy run start

# IP/Vlan configuration		
## Enter interface configuration mode for *interface*
- Host Configuration Mode
	- inteface *interface*
		
## Set the ipv4 address and subnet mask of the current interface
- Interface Configuration Mode
	- ip address *ip address* *subnet mask*

## Set the ipv6 address and subnet mask (in / suffix form) of the current interface
- Interface Configuration Mode
	- ipv6 address *ipv6 address*/*subnet mask*

## Give the current interface a description
- Interface Configuration Mode
 	- description *description*

## Enable the current interface
- Interface Configuration Mode
	- no shutdown

## Set the current interface to full duplex
- Interface Configuration Mode
	- duplex full

## Set the speed of the current interface in Mbps (Megabits per second)
- Interface Configuration Mode
	- speed *speed value*

## Set the current interface to use the auto-MDIX feature
- Interface Configuration Mode
	- mdix auto

## Set the default gateway of a switch
- Host Configuration Mode on Switch
	- ip default-gateway *default gateway*

## Create a loopback interface and enter interface configuration mode for the loopback interface
- Host Configuration Mode , Router
	- ip address *ip address* *subnet mask*

## Create a VLAN with a valid ID number if no vlans with that ID already exist, and enter vlan configuration mode for that vlan
- Host Configuration Mode
	- vlan *vlan-id*

## Give a vlan a specific name
- Vlan Configuration Mode
	- name *name*

# Secure Shell Commands
## Verify SSH (Secure Shell) Support
- Privileged Executive Mode
	- show ip ssh

## Configure IP domain-name
- Privileged Executive Mode
	- ip domain-name *domain name*

## Move to SSH (Seure Shell) Version Two
- Global Configuration Mode
	- ip ssh version 2

## Enable SSH server and generate RSA key pairs
- Global Configuration Mode
	- crypto key generate rsa

## Configure SSH (Secure Shell) Username and Password
- Global Configuration Mode
	- username *username* secret *password*

## Enter line configuration mode for lines 0-15. Used in conjunction with the following commands to enable ssh.
- Global Configuration Mode
	- line vty 0 15

## Enable SSH on current lines
- Line Configuration Mode
	- transport input ssh
   	  login local

## Check if SSH is enabled
- Privileged Executive Mode
	- show ssh

# Diagnostic Commands
## View the auto-MDIX settings of a specific interface
- Privileged Executive Mode
	- show controllers ethernet-controller *interface* phy | include MDIX

## Display Interface status and Configuration
- Privileged Executive Mode
 	- show interfaces *interface*

## Display Current Startup configurations
- Privileged Executive Mode
	- show startup-config : show start

## Display current running configuration
- Privileged Executive Mode
	- show running-config : show run

## Display information about flash file system
- Privileged Executive Mode
	- show flash

## Display Hardware and software status
- Privileged Executive Mode
	- show history

## Display MAC address table
- Privileged Executive Mode
	- show mac-address-table : show mac address-table

## View status of ipv4 interfaces
- Privileged Executive Mode
	- show ip interface brief

## View status of ipv6 interfaces
- Privileged Executive Mode
	- show ipv6 interface brief

## View the ipv4 routing table
- Privileged Executive Mode
	- show ip route

## View the ipv6 routing table
- Privileged Executive Mode
	- show ipv6 route

## Set the number of lines of text displayed at once by the various "show" commands
- Privileged Executive Mode
	- terminal lenght *lines*

## Ping an device with the specified IP address
- Privileged Executive Mode
	- ping *ip address*

# Boot Loader Commands
## View position of boot environment variable
- Boot Loader Mode
	- set

## Initalize flash file system
- Boot Loader Mode
	- flash_init
		
## View files in flash file system
- Boot Loader Mode
	- dir flash:

## Change the path of the boot environment variable to *file path*
- Boot Loader Mode
	- BOOT=flash:*file path*
		
