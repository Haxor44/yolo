# Stage 2 Implementation of Ansible And Terraform(OPTIONAL)
This repository provides a solution to automate the provisioning of cloud resources using Terraform(optional) and the subsequent configuration of these resources using Ansible, all triggered from a single Ansible playbook.

## Prerequisites
### Before you begin, ensure you have the following installed on your local machine:

### 1. Terraform
### 2. Ansible
### 3. Python
### 4. AWS CLI (if using AWS)


## Ansible Playbook for Provisioning and Configuration
### The Ansible playbook provided in this repository handles both the provisioning of resources using Terraform and the configuration of those resources.

## Ansible Playbook for Provisioning and Configuration
### The Ansible playbook provided in this repository handles both the provisioning of resources using and the configuration of those resources on vagrant server.

### Update Inventory

#### 1. Before running the playbook, ensure your ansible/inventory.ini file is correctly set up. This file may be dynamically updated during the provisioning process.

#### 2. Run the Ansible Playbook
#### using the following command ansible-playbook -i hosts -c ssh playbook.yaml

#### The playbook will:

#### Provision the necessary  resources e.g. setup node, mongdb and launch application on vagrant server using Ansible roles.
