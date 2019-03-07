### COSC6377 Project Proposal
#### Stuart Baxley
#### Spring 2019

#### Title
Expanding VTS to Control Remote OVSDB Servers

#### Problem 
Virtual topology services,[^1] VTS, is a container and virtual switch orchestration software system. VTS interfaces with docker to create and manage containers as well as Open Vswitch, OVS, to manage the connectivity between the containers on the local machine. VTS writes configuration changes to the local OVSDB server. Currently, VTS is limited to orchestration within the local machine on which it is running.

#### Solution
I propose expanding the capabilities of VTS by adding the ability to write configuration changes to remote OVSDB servers. This will enable a centralized VTS to control resources on physical switches as well as OVS instances on other compute nodes. In addition to pushing configuration, this project will enable collection of statistics, statuses, and capabilities of these devices.

#### Networking Component
* OVSDB RPC semantics
* Virtual networking with Pica8 switch
* Creating/using SSL certificates
* API programming

#### Milestones
##### End of March
1. Establish communication with OVSDB server on remote machine
2. Enable SSL to secure communications (this may be required before previous step)
3. Incorporate remote OVSDB control with current OVS system calls and RPC’s
##### End of April
4. Expand OVS capabilities in VTS to include different capabilities of physical switch vs virtual switch
5. Test functionality and create demo
6. Complete report

#### Future Work
This project will be further expanded to remotely interact with docker servers for container orchestration on remote hardware. 

[^1]: https://bitbucket.org/barnstorm/vts
