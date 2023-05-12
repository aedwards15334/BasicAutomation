Basic Automation with Ansible This repo should be looked at through the lens of time and software versions.

This will help you avoid frustration if somthing doesn't work.

I created the repo 5/12/23 with the following baseline software versions:

GNS3 2.2.28 VM and Desktop 

From the GNS3 marketplace:
  GNS3 c8000v appliance
    IOS-XE 17.06.01a 8G serial (c8000v-universalk9_8G_serial_17.06.01a.qcow2) 
  GNS3 Network Automation Container
    adosztal/network_automation IMAGEID: dd6864157ed4 

VMware Workstation 15 Pro
  Version: 15.5.7 build-17171714

The following updates to the original network automation container through the lab:

Pulled the docker image adosztal/network_automation as part of the network automation appliance on GNS3 marketplace

Perform the following updates on the network automation appliance/container:
  apt update 
  apt remove ansible 
  apt install ansible 
  apt install sshpass 
  apt install python3-pip 
  pip install ansible-pylibssh 
  apt autoremove ansible-galaxy collection install -f cisco.ios cisco.nxos cisco.asa cisco.ise

The software versions applied and relevant through this process at the time were: 
Ubuntu 18.04 (uname -r -> 5.0.0-37-generic) 
ansible -version ([core 2.12.10) 
ansible-galaxy collection list 
  cisco.ios 4.5.0 
  cisco.asa 4.0.0 
  cisco.ise 2.5.12 
  cisco.nxos 4.3.0 
  ansible.netcommon 5.1.1 
  ansible.utils 2.10.1 
python3 --version (v 3.8.10) 
sshpass -V (v 1.06) 
pip -V (v 20.0.2) 
pip list ansible-pylibssh (v 1.1.0)

Good luck and Happy Automating!

