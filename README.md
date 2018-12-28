# Objective

For this guide we are going to setup the playbook to establish passwordless SSH logins with the remote hosts. Passwordless logins is a great convenience when connecting to multiple servers.

# Ansible reference

Ansible installed on your local machine. For installation instructions, follow the official Ansible installation documentation.
Familiarity with Ansible playbooks. For review, check out Configuration Management 101: Writing Ansible Playbooks.

# Download the tool

Clone the repository to your ansible-enabled host:
https://github.com/henshitou/ansible-ssh.git

# Prerequisites

Check below command are available to the PATH of the user you will be running the playbook as.

ssh-keygen
ssh-copy-id
sshpass

# Preparations before you run
Edit the hosts file and define your environment's information
  ## ssh_key_filename	
the filename of the new SSH key to be generated and stored under your .ssh folder of your localhost.
  ## remote_machine_username
the username of the remote machines. If you are applying the procedure to multiple hosts.
  ## remote_machine_password
the password of the "remote_machine_username" remote machines.
  ## ansible_setup_passwordless_setup_group
fill in the list of hosts that you want to establish the passwordless login with.

# How to run it

Execution command 
ansible-playbook -i hosts ansible_ssh.yml
