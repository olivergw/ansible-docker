# Ansible-Docker
## Docker and Docker Compose Installation Playbook

I wrote and tested this script on Ubuntu 14.04 only.

This ansible playbook has only come about as I have recently found myself installing Docker and Docker Compose constantly for testing. 

Simply update the hosts file with the IP or names of your target servers and then run:

````$ ansible-playbook -i hosts site.yml````