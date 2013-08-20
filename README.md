ecgps-ansible
=============

provision, configure, and deploy ecgps using ansible


SETUP
=====

- install ansible
   - sudo pip install ansible
   - sudo apt-get install ansible
   - other methods - http://www.ansibleworks.com/docs/gettingstarted.html


EXAMPLE
=======

- ansible-playbook -u root -k -i dev_servers site.yml


NOTES
=====
- You will need to know the root password of the machine you are trying to setup the '-k' option prompts you for your
password

- Ensure that your host machine has the necessary public key authentication setup to access the ecgps github repo



