# AbuDhabiTest
Repository for the Abu Dhabi Test 

In this project a playbook was created for the automation of the next processes: 

1. Docker download with the necessary dependencies.
2. Sonarqube and Postgresql docker containers downloads. 
3. Deployment of Sonarqube docker container to work with Postgresql as its database. 

Deployment

1. On the EC2 instance there were four steps performed manually:  

1.1 The update of the OS packages with the "yum update" command. 

1.2 The installation of ansible in the EC2 instance.

1.3 The creation of the ansible user in order to run the playbook (The ansible user was added to the "wheel" group for sudo privileges).

1.4 The creation of a directory called play for the playbook.

2. The next step of the process is running the playbook named "playbooksonar.yaml". The command used for this was "ansible-playbook -u ansible playbooksonar.yaml". 

The playbook contains two plays: 

1. The first play is for the installation of docker and initialization of the service.  

2. The second play is for installing and setting up the requirements of the sonarqube and postgresql docker containers. In the setting up there's the configuration for sonarqube to use postgresql as its database.


