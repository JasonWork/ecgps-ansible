ecgps-ansible
=============

provision, configure, and deploy ecgps using ansible


SETUP
=====

- Install ansible
   - sudo pip install ansible
   - sudo apt-get install ansible
   - other methods - http://www.ansibleworks.com/docs/gettingstarted.html

- Update the file 'dev_servers' with a user name and the address of the remote machine

- Optionally update the file 'all.yml' in the 'group_vars' directory. You should at least review this file as it acts
as a config file

- Run this command from the directory where you cloned the repo
    ansible-playbook -u root -k -i dev_servers site.yml

- Once the playbook has finished you can ssh to the remote machine as the user defined in the 'all.yml' file

- To run the ecgps app you can do:

    load fixtures
    ./create_branch_database.sh

    If you did not install on localhost you can:
    ./manage.py runserver <SERVER>:8000


NOTES
=====

- You will need to know the root password of the machine you are trying to setup the '-k' option prompts you for your
password.

- Ensure that your host machine has the necessary public key authentication setup to access the ecgps github repo.

- Currently used for setting up development machines using Ubunutu. Will be updated in the future for other linux
machines and non development purposes.




