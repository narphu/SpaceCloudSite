## Overview
This project provides a simulation environment that can be used to evaluate a scalable collection of Global Network Access Terminals (GNATs), a concept under investigation as part of the Space Combat Cloud Project.
<img src="https://raw.githubusercontent.com/nprabhu2195/SpaceCloudSite/master/Imageforwebsite.jpg">
The environment is used to simulate a mesh network of satellites/GPS systems connected to work in tandem. Docker containers are used to represent each satellite and OVS is used to interconnect them to form a communication network. Each satellite encloses multiple nested Docker containers designated to act as components and interconnected via OVS. 


## News and Releases

### 07-11-2019: 

Supports 32-node simulation for a long duration simulation. Source code of the components changed to support multiple satellite communication over several time slots. Minor bug fixes.

[Release Document Version 2.0](https://github.com/nprabhu2195/SpaceCloudSite/blob/master/spacecloud-sim_doc2.0.pdf)

[Release VM Version 2.0](https://drive.google.com/drive/folders/1O8I_HlIIV7AfLQYlbiITgpC0-AUNQ6qu?usp=sharing)

### 03-15-2019: 
Version able to support four node simulation using bash terminals and for one time slot.

[Release Document Version 1.0](https://github.com/nprabhu2195/SpaceCloudSite/blob/master/spacecloud-sim_doc1.0.pdf)

[Release VM Version 1.0](https://drive.google.com/drive/folders/1Q4xO22gOut770oWz0WkOZw57l22u55Gf?usp=sharing)

### Bitbucket Source Code Repository

[Latest Source Code](https://bitbucket.org/DawnZhang/airforce/src/develop/)

_Note: The code in GNAT_Docker is under constant development from our partner developer. Some changes might lead to bugs or errors if running the simulator using the old json files/mastercontroller/scripts and new source code. We are constantly trying to update the files to maintain uniformity across all the aspects of the emulator. We apologise for any inconvenience caused in advance._

### Prerequisites

An Ubuntu 16.04 operating system is necessary to run the simulator, as the newest version does not support the Linux kernel modules and Linux-headers dependencies needed for the OpenvSwitch installation. The kernel version used was 4.4.0.138. Older kernel versions might add arbitrary padding to UDP raw packets and cause data communication checksum issues. 

```markdown
Build the emulator using the scripts

# Build a 32-node emulator with docker containers
Use scripts from the /home/Airforce/airforce/scripts directory in the VM
./env_setup.sh -s 31 -p 4 -g 1

# Clear the 32-node emulator
./env_clear.sh -s 31 -p 4 -g 1

Other commands are elaborated in the document
```

### Support or Contact

For any questions shoot a mail at: nprabhu@umass.edu.
