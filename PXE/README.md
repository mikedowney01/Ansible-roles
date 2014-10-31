PXE
=======
```
$ ansible-playbook -i hosts site.yml
```
will provision a PXE server with the IP 10.1.2.4 by default.
Boot another machine from LAN on the same network to install Ubuntu on that machine.

Variables
=======
The variables in host_vars/PXE will need to be changed for your environment.
Ensure that ansible_ssh_private_key_file and ansible_ssh_user 
are uncommented before running the playbook.

Vagrantfile
=======
```
$ vagrant up
```
will provision a vm in VirtualBox with the IP 10.1.2.4 by default.
Ensure that ansible_ssh_private_key_file and ansible_ssh_user
are commented out.

A client vm will need to be created with the network card on the same "host only"
network as the PXE server.
