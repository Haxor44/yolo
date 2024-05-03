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

Configure volumes, networks, and environment variables as needed. In this case the newtork created was yolo_net where all the services communicate with each other and the volume created was data for the mongodb

Define ports mappings for accessing services externally.


### 7. Test with docker-compose
Use `docker compose build` to build and `docker compose up` to start the containers defined in the docker-compose.yml file.

Verify that all services are running correctly and communicating with each other.

Test the application's functionality thoroughly.


