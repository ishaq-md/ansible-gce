Automate Instance and Apache Server on GCP using Ansible
Description
The goal of this repository is to create a instance on GCP and deploy apache server on that instance using ansible playbook.

Prerequisites
Create Project on Google Cloud Platform.
Create a Serviceaccount with editor access. (Refer Creating-service-account)
Getting Started !!
Install python version > 3.0
$ sudo yum install python3-pip
The GCP modules require both the requests and the google-auth libraries to be installed.
$ sudo pip3 install requests google-auth
Install Ansible
$ sudo pip3 install ansible 
Download .JSON credentials file of created service account.
Edit instance_name in vars/main.yml, by default it is centos-7.
Edit machine_type in vars/main.yml, by default it is e2-micro.
Edit zone in vars/main.yml, by default it is us-central1-a.
Edit source_image in vars/main.yml, by default it is CENTOS-7.
Give project id, .JSON file_path in vars/main.yml file.
Run the Playbook
$ ansible-playbook gce.yml
Your Google Compute Engine Instance is now created, with Apache Server installed in it.
Browse to instance public ip address.
