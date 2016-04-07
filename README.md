# Ansible-Change-Hostname
Consists of two tasks: 1) Uses Ansible's buitin 'Hostname' module to modify hostname and 2) Uses the 'Replace' module to update the /etc/hosts file

In this example, one server is defined in the hosts file along with it's desired hostname (server1), it's IP address and 'ssh_user' to indicate what user to login with.

site.yml is the top level playbook which includes servers.yml. Common to all servers are the 'Change Hostname' tasks which are defined in role/common/tasks/main.yml 

To run, edit the hosts file to point to a valid server, set a desired hostname (currently 'server1') and run: ansible-playbook site.yml --ask-sudo-pass --sudo
