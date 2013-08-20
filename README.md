ecgps-ansible
=============

provision, configure, and deploy ecgps using ansible


SETUP
=====

- install ansible
   - sudo pip install ansible
   - sudo apt-get install ansible
   - other methods - http://www.ansibleworks.com/docs/gettingstarted.html

- update the file 'dev_servers' with a user name and the address of the remote machine

EXAMPLE
=======

- ansible-playbook -u root -k -i dev_servers site.yml


NOTES
=====

- You will need to know the root password of the machine you are trying to setup the '-k' option prompts you for your
password.

- Ensure that your host machine has the necessary public key authentication setup to access the ecgps github repo.

- Currently used for setting up development machines using Ubunutu. Will be updated in the future for other linux
machines and non development purposes.




