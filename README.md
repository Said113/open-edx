# Open edX Devstack
## Devstack Installation : A Step by Step Complete Guide
------------------------------------

#### This just for linux
### Getting Started

Step 0:
  - sudo apt update
  - sudo apt upgrade

Step 1:
  - sudo apt install docker.io
  - sudo apt install make
  - sudo apt install git

Step 2:
  - docker info | grep -i 'storage driver'      -------> the output here must be "overlay2"
  - mkdir openedx
  - cd openedx

Step 3:
  - git clone https://github.com/edx/devstack
  - cd devstack
  - git checkout open-release/hawthorn.master
  - export OPENEDX_RELEASE=hawthorn.master

Step 4:
  - sudo apt install curl
  - sudo curl -l "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /u(sr/local/bin/docker-compose
  - sudo chmod +x /usr/local/bin/docker-compose
      
Step 5:
  - make dev.checkout
  - make dev.clone
  - make dev.provision
  
# Run your Open_edX (Devstack) Platform
Step 6:                                                     
  - sudo docker-compose up       -------> here you must be run this command in the path where docker-compose file exist
  - sudo make dev.up             -------> i recommend to use this command to Run your Platform 
  
# Access to your Open_edX (APP) 
### to access your CMS 
  - go to your browser and set this URL http://localhost:18000/ 
  
### to access your LMS 
  - go to your browser and set this URL http://localhost:18010/
  
### to access your Django ADMIN
  - go to your browser and set this URL http://localhost:18000/admin/
  - user is: edx
  - motepass is : edx

# Stop your Open_edX (Devstack) Platform
Step 7:
  - sudo docker-compose down     -------> here you must be run this command in the path where docker-compose file exist


