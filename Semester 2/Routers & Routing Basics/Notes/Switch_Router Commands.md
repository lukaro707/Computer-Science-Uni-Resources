## Command Syntax:
# Description of command and parameters
	- Command pre-requisites (mode, device, etc.)
		- command *parameter* : alternatecommand *parameter*

# Enter Privileged Exectuive Mode
	- User Exectuive Mode
		- enable
		
# Enter Host Configuration Mode
	- Privileged Executive Mode
		- configure terminal : config t

# Change the path of the boot environment variable to *file path*
	- Host Configuration Mode
		- boot *file path*
		
# Enter interface configuration mode for *interface*
	- Host Configuration Mode
		- inteface *interface*
		
# Set the ipv4 address and subnet mask of the current interface
	- Interface Configuration Mode
		- ip address *ip address* *subnet mask*

# Set the ipv6 address and subnet mask (in / suffix form) of the current interface
	- Interface Configuration Mode
		- ipv6 address *ipv6 address*/*subnet mask*

# Enable the current interface
	- Interface Configuration Mode
 		- no shutdown

# Set the current interface to full duplex
	- Interface Configuration Mode
 		- duplex full

# Set the speed of the current interface in Mbps (Megabits per second)
	- Interface Configuration Mode
 		- speed *speed value*

# Set the current interface to use the auto-MDIX feature
	- Interface Configuration Mode
 		- mdix auto

# Set the default gateway of a switch
	- Host Configuration Mode on Switch
 		- ip default-gateway *default gateway*

# Return to Privileged Executive Mode
	- Any mode higher than Host Configuration Mode
 		- end

# View status of ipv4 interfaces
	- Privileged Executive Mode
 		- show ip interface brief

# View status of ipv6 interfaces
	- Privileged Executive Mode
 		- show ipv6 interface brief

# View the auto-MDIX settings of a specific interface
	- Privileged Executive Mode
 		- show controllers ethernet-controller *interface* phy | include MDIX

# Display Interface status and Configuration
	- Privileged Executive Mode
 		- show interfaces *interface*

# Display Current Startup configurations
	- Privileged Executive Mode
 		- show startup-config : show start

# Display current running configuration
	- Privileged Executive Mode
 		- show running-config : show run

# Display information about flash file system
	- Privileged Executive Mode
 		- show flash

# Display Hardware and software status
	- Privileged Executive Mode
 		- show history

# Display MAC address table
	- Privileged Executive Mode
 		- show mac-address-table : show mac address-table

# Save the current running configuration to the startup configuration
	- Privileged Executive Mode
 		- copy running-config startup-config : copy run start

# View position of boot environment variable
	- Boot Loader Mode
		- set

# Initalize flash file system
	- Boot Loader Mode
		- flash_init
		
# View files in flash file system
	- Boot Loader Mode
		- dir flash:

# Change the path of the boot environment variable to *file path*
	- Boot Loader Mode
		- BOOT=flash:*file path*
		
