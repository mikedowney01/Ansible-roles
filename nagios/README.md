nagios
=======
```
$ ansible-playbook -i hosts site.yml
```
will provision a nagios server with the IP 10.1.2.4 by default.
The web interface can be accessed via http://10.1.2.4/nagios
with username "nagiosadmin" and password "nagiosadmin"

Variables
=======
The variables in host_vars/nagios will need to be changed for your environment.
Ensure that ansible_ssh_private_key_file and ansible_ssh_user 
are uncommented before running the playbook.

Vagrantfile
=======
```
$ vagrant up
```
will provision a vm in VirtualBox with the IP 10.1.2.4 by default.
Ensure that ansible_ssh_private_key_file and ansible_ssh_user are commented out.
