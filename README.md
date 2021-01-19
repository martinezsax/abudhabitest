# AbuDhabiTest
Repository for the Abu Dhabi Test 

In this project a playbook was created for the automation of the next processes: 

1. Docker download with the necessary dependencies.
2. Sonarqube and Postgresql docker containers downloads. 
3. Deployment of Sonarqube docker container to work with Postgresql as its database. 

Deployment

1. On the EC2 instance there were three steps performed manually, the update of the OS packages with the "yum update" command, the creation of the ansible user in order to run the playbook (The ansible user was added to the "wheel" group for sudo privileges) 

2. The next step of the process is running the playbook named "playbooksonar.yaml". The command used for this was "ansible-playbook -u ansible playbooksonar.yaml".


