# Changes to PiView-AG
## TO DO
This is a list of components to be implemented:

- **HARDWARE**: camera statuses
- **HOST**:  name
- **NETWORK**: host name, interface names, ip addresses, mac addresses
- **STORAGE**: total disk capacity, free disk capacity, total RAM and free RAM
- **CPU**: load across each core of the processor (as a list/dictionary)

Future features will be added to this list as required.

## COMPLETE
These items are completed.

### 0.4.0 Network Features
The following are implement in this version:
- host name
- interface names
- ip addresses
- mac addresses

Fixed missing self references in classes, removed get_ from function names
Added missing file headers...

### 0.3.0 Host Features
The following have been implemented:
- boot time 
- model
- serial number
- uptime
- revision


- ### 0.2.0 Hardware Features
Added Hardware checking for:
	- SPI
	- I2C
	- BT
Updated [[README]]
Design and added PiView Icon

- ### 0.1.1 GPU Features
Added:
	- GPU temperature

- ### 0.1.0 CPU Features
Added:
	- max load across cores
	- processor temperature
	- processor clock speed

- ### 0.0.3 Setup fixes
Small fixes to setup.cfg, and a source reformat.

- ### 0.0.2 Utils
Added Utils to the package. Utils includes:
	- format_bytes
	- draw_line

- ### 0.0.1 Initial Version
Blank project, containing:
	- starter folder structure
	- [[README]]  
	- [[CHANGES]]
	- [[LICENSE.txt]]