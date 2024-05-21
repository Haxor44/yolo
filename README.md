# Prerequisites
Ensure you have Docker and docker-compose installed on your system. If not, follow the official Docker documentation for installation instructions.

## Steps
### 1. Understand Application Requirements
Analyze the application requirements and dependencies.

Determine which services need to be containerized and their configurations.

### 2. Create Dockerfiles
For each service, create a Dockerfile.
Specify base images, dependencies, environment variables, and commands to run the service.

Optimize Dockerfiles for size and efficiency by minimizing layers and leveraging multi-stage builds.

### 3. Customize Dockerfiles
Tailor Dockerfiles based on the specific needs of each service.

Install additional packages or dependencies if required.

Configure environment variables for different environments (development, testing, production)


### 4. Build Docker Images
Build Docker images using the `docker build` command.

Tag images appropriately for easy identification in this case the tags for the images were haxor44/client:v1.0.0 for the react client app and haxor44/backend:v1.0.0 for the node backend.

### 5. Test Docker Images
Test the built Docker images locally to ensure they function as expected.

Debug any issues that arise during testing.

### 6. Create docker-compose.yml
Define services and their configurations in the docker-compose.yml file.

Specify image names or build contexts for each service.

Configure volumes, networks, and environment variables as needed. In this case the newtork created was yolo_net where all the services communicate with each other and the volume created was data for the mongodb.

Define ports mappings for accessing services externally.


### 7. Test with docker-compose
Use `docker compose build` to build and `docker compose up` to start the containers defined in the docker-compose.yml file.

Verify that all services are running correctly and communicating with each other.

Test the application's functionality thoroughly.

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

# Stage 2 Implementation of Ansible And Terraform
This repository provides a solution to automate the provisioning of cloud resources using Terraform(optional) and the subsequent configuration of these resources using Ansible, all triggered from a single Ansible playbook.

## Prerequisites
### Before you begin, ensure you have the following installed on your local machine:

### 1. Terraform
### 2. Ansible
### 3. Python
### 4. AWS CLI (if using AWS)


## Ansible Playbook for Provisioning and Configuration
### The Ansible playbook provided in this repository handles both the provisioning of resources using Terraform and the configuration of those resources.

### Update Inventory

#### 1. Before running the playbook, ensure your ansible/inventory.ini file is correctly set up. This file may be dynamically updated during the provisioning process.

#### 2. Run the Ansible Playbook
#### using the following command ansible-playbook -i hosts -c ssh playbook.yaml

#### The playbook will:

#### Execute Terraform to provision the necessary cloud resources.
#### Use the output from Terraform to update the Ansible inventory.
#### Configure the provisioned servers using Ansible roles and tasks