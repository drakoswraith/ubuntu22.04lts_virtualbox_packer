# ubuntu2204lts_virtualbox_packer
Basic Packer build for Ubuntu 22.04LTS using the VirtualBox ISO builder

Features / approach
- SSH Communicator
- NAT network (bridged approach commented out)
- Installs the VirtualBox Guest Additions
- user-data passed via CDROM method

Login 
Username and password are "packer"

Ubuntu 22.04 updated the boot menu from 20.04, causing the packer build sequence to require updating.
ssh_handshake_attempts needed to be increased as well (and the stopping of SSH in the user-data is a key requirement to prevent the timeout from starting to soon)
