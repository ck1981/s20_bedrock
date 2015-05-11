# s20_bedrock
##s20.com Wordpress Bedrock site on Windows host

This is a standard working setup using the Bedrock stack (one exception below), i.e. Bedrock based WordPress LEMP app server running on Vagrant VM provisioned by Ansible. It is running on a Windows host machine (8.1).

C:\s20\ansible\roles\wordpress-install\tasks\main.yml - 'Create .env file' task expanded due to issue with writing to the folder shared between the Windows host machine and the VM.

Currently using default theme.

Currently during provisioning Ansible seems not to find the 'roles-path' varible in the ansible.cfg file and indeed may not be reading the entire file in the project directory and rather the ansible.cfg in the default location (etc/ansible?). The external Ansible roles were therefor installed into ansible/roles with the intention of adding them to the .gitignore file (which has not been done during the initial commit).
