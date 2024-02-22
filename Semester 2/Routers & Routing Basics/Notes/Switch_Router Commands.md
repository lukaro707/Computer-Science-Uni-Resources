# Command Syntax:
- Description of command and parameters
	- Command pre-requisites (mode, device, etc.)
		- command *parameter* : alternatecommand *parameter*

- Enter Privileged Exectuive Mode
	- User Exectuive Mode
		- enable
		
- Enter Host Configuration Mode
	- Privileged Executive Mode
		- configure terminal : config t

- Change the path of the boot environment variable to *file path*
	- Host Configuration Mode
		- boot *file path*
		
- Enter interface configuration mode for *interface*
	- Host Configuration Mode
		- inteface *interface*
		
- Set the ipv4 address and subnet mask of the current interface
  - Interface Configuration Mode
		- ip address *ip address* *subnet mask*

- Set the ipv6 address and subnet mask (in  suffix form) of the current interface
	- Interface Configuration Mode
	  - ipv6 address *ipv6 address* *subnet mask*
		
- View position of boot environment variable
	- Boot Loader Mode
		- set

- Initalize flash file system
	- Boot Loader Mode
		- flash_init
		
- View files in flash file system
	- Boot Loader Mode
		- dir flash:

- Change the path of the boot environment variable to *file path*
	- Boot Loader Mode
		- BOOT=flash:*file path*
		
