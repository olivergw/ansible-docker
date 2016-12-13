# Ansible-Docker

Written for CentOS 7 and Ubuntu 14.04-05 only.

This ansible playbook has only come about as I have recently found myself installing various applications quite frequenty and across different distibutions.

**Current Roles:**

**Common** - Installs various useful services, IPTables, NTP etc...

**Docker** - Installs the latest version of Docker from apt or yum and also installs Docker-Compose.



Simply update the hosts file with the IP or names of your target servers under each app you require:

````
[common]
192.168.77.162

[docker]
192.168.77.162
````

Then run: 

````
$ ansible-playbook -i hosts site.yml
or
$ ansible-playbook -i hosts site.yml --ask-pass --become --ask-become-pass
````

Inside the root directory there is an ansible.cfg file, this includes a few lines for fast caching results from *gather_facts.* This means as each playbook is run the facts can be reused and not incur a hefty wait while it goes to collect them again.
