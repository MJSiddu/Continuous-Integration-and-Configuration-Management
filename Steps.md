# Steps to Run

## Install required tools

* Install VirtualBox
* Install Virtual Machine

## Setup Project

### Perform the following inside the Virtual Machine

Install Ansible:
* $ `sudo apt-add-repository ppa:ansible/ansible`
* $ `sudo apt-get update`
* $ `sudo apt-get install ansible`

Add all the required files to the root directory ("/home/siddumj21"):
* roles.yml
* playbook.yml
* inventory


PING - localhost in our case:
* $ `ansible all -m ping -i inventory`

### Run roles.yml using ansible-playbook command to create/install roles:
* $ `ansible-playbook roles.yml`

### Run playbook.yml using ansible-playbook command:
* $ `ansible-playbook playbook.yml -i inventory`

Now check if the app is running properly on the forever server: 
* run $ `forever list` - this should list our running app on port 3090
* Open Chrome and go to `192.168.33.1:3090` and we should see the home page of the application.


