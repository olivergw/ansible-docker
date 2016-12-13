# Ansible-Common
## Collection of different roles in one playbook

I wrote and tested this script on CentOS 7 and Ubuntu 14.04 only.

This ansible playbook has only come about as I have recently found myself installing various applications quite frequenty and across different distibutions.

**Current Roles:**

**Common** - Installs various useful services, IPTables, NTP etc...


**Docker** - Installs the latest version of Docker from apt or yum and also installs Docker-Compose.

**MongoDB** - Installs a standalone MongoDB service


Simply update the hosts file with the IP or names of your target servers under each app you require:

````
[common]
192.168.77.162

[docker]
192.168.77.162

[mongo]
192.168.77.162
````

Then run: 

````
$ ansible-playbook -i hosts site.yml
````

Inside the root directory there is an ansible.cfg file, this includes a few lines for fast caching results from *gather_facts.* This means as each playbook is run the facts can be reused and not incur a hefty wait while it goes to collect them again.
