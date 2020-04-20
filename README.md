# Deploy JPetStore demo setup to an UCD Server

This playbook will deploy the JPetStore Demo artifacts (db definitions, UCD app definitions, and so on) into an existing UCD server. 
It needs the group variables from https://github.com/osmanburucu-ibm/deploy-urbancode-deploy to work. 
Recommended setup is:

~~~sh

mkdir ucd_demo_setup
cd ucd_demo_setup
git clone https://github.com/osmanburucu-ibm/deploy-urbancode-deploy.git
git clone https://github.com/osmanburucu-ibm/deploy-jpetstore-demo.git

~~~~

Edit deploy-urbancode-deploy/hosts to set the hostname and ip of your ucd server and run the setup-all-ucdsa.yml to setup your UCD environment.

Edit the variables to point to the location where the artifacts are stored.

Then run the playbook from here to setup the JPetStore Demo

~~~sh 
 ansible-playbook setup-jpetstore-demo.yml -i hosts -u <your ansible ssh user>
~~~