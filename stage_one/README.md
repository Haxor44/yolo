# Stage 1 Using Ansible and Vagrant
This repository provides a solution to automate the provisioning of  resources using vagrant and the subsequent configuration of these resources using vagrant and Ansible and is triggered from a single Ansible playbook or using vagrant up.
## Prerequisites
### Before you begin, ensure you have the following installed on your local machine:

### 1. Vagrant
### 2. Ansible

## Ansible Playbook for setting up docker and clone repository containing web app
### The Ansible playbook will install docker and docker compose on the vagrant machine and then clone the repository and run the app

### Vagrant in this case was used to port forward ports so that hte app can be accessed from host machine as well as setup the playbook to run

### use vagrant up to run the application.