# Stage 1 Using Ansible and Vagrant
This repository provides a solution to automate the provisioning of  resources using vagrant and the subsequent configuration of these resources using vagrant and Ansible and is triggered from a single Ansible playbook or using vagrant up.
## Prerequisites
### Before you begin, ensure you have the following installed on your local machine:

### 1. Vagrant
### 2. Ansible
### 3. Virtualbox

## Ansible Playbook for setting up docker and clone repository containing web app
### 1. The Ansible playbook will install docker and docker compose on the vagrant machine.
### 2. The playbook will  then clone the repository containing the source code.
### 3. In the final step the ansible will the run docker-compose on the vagrant machine and lauch the application.

### Vagrant in this case was used to port forward ports so that the app can be accessed from host machine as well as setup the playbook to run.

### use vagrant up to run the application.