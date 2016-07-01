# f5_ansible

Problem this snippet solves:
While everyone loves F5, we all know the initial system setup, networking components and device service cluster is a tedious process. This simple Ansible playbook will allow you to automate the entire F5 initial setup by reading a CSV file and leave you with a ready to go active/standby pair.

This does include setting up - NTP, DNS, Hostname, LACP, dot1q, Self-IPs, device trust, configuration sync, etc

How to use this snippet:
How to Use

Required Items

Ansible (tested on version 2.1)
Blank pair of F5s with management IP configured (version 12.0 & 12.1)
Install Ansible if Needed

Official Ansible Install Guide
http://docs.ansible.com/ansible/intro_installation.html

Great 3rd Party Install Guide
https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-14-04

Download and Run F5 Ansible Setup Playbook - f5_ansible_setup.yml
https://github.com/mwallco/f5_ansible/blob/master/f5_ansible_setup.yml

Please run the following Ansible Playbook. This will download the required modules, playbook for F5 Initial Setup and example CSV file. Be sure to run this playbook from ~/ansible/playbooks/

F5 Ansible Setup Playbook

Fill Out CSV File - f5_initial_setup.csv

Use the example CSV file as an example to fit to your environment. Using the CSV file allows you to not have to edit the actual F5 Initial Setup Playbook. This was tested on a pair of 5200v's with so adjust interfaces as needed. The CSV file will be automatically downloaded from GitHub when you run the F5 Ansible Install Playbook.

Run F5 Initial Setup Playbook - f5_initial_setup.yml

Once you have edited the CSV file to your needs, run the F5 Initial Setup Playbook. This playbook will read the CSV file and configure the two F5 devices from scratch. When everything completes, you should be left with an active/standby pair of devices ready to go!

If you want to manually install the Ansible Playbook & Modules, please check out - GitHub

Tested on Version:
12.0 & 12.1
