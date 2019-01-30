# docker-configuration-management
A simple way to manage separate configuration for different environment.

# How to manage docker configuration for dev ,stage or prod separately
Writing a docker-compose.yml to run the service is easy but maintaining the configuration based on the environmnet might be a bit challenging. It is not a good idea to have same configuration for dev and produciton server. To make it even simpler, we don't turn on debugger for production server. 

# Simple docker-compose to separate the environment based on docker container.

I love simplicity and want to learn from the simplest and practical example. The best I can assume will be to setup a mysql container and setting up a database and credential for it. We will setup a differnet username and password for dev and prod.

# To run the container for dev environment run the base docker-compose.yml and the dev-docker-compose.yml
the naming convention can be different depending upon your ease but we must need one docker-compose.yml file.

`docker-compose -f docker-compose.yml -f dev-docker-compose.yml up -d`

# To the run the container for Prod server
`docker-compose -f docker-compose.yml -f prod-docker-compose.yml up -d`

Now, we have two container one can be to server the development environment and one can be used to serve the production. Make the changes depending upon your requirement. This is just a simple example
