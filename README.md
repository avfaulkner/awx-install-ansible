# Install AWX Software and Dependencies
### This playbook is based on the instructions and requirements listed in the [Official AWX Repo](https://github.com/ansible/awx)

## About
AWX is an automation tool that allows you to manage Ansible playbooks, inventories, and schedule jobs to run using the web interface.

AWX is the open source version of [Ansible Tower](https://www.ansible.com/products/tower)

## Requirements
### Tooling
- Ansible >= 2.9.10

## Instructions
1. Clone the repository to your local machine
2. What host will you install AWX on? Add the host details in hosts.ini 
3. Add your desired variables in vars/main.yml
 -  *IMPORTANT*: the "target_host" variable in vars/main.yml must be set to one of the host headings listed in hosts.ini (local, awx-centos, awx-ubuntu) to install AWX on that host. 
4. Run the playbook
 ```
 ansible-playbook -i hosts.ini main.yml
 ```