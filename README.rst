======================================================
A Simple Ansible Role for Installing Cloudmesh_Client
======================================================

This Ansible Role will install Cloudmesh-Client in the hosts specified in the hosts file

======================================================
Installing Ansible in your local System
======================================================
Assuming you have pip installed ( Mac OSX )
  sudo pip install ansible

Install the epel-release RPM if needed on CentOS, RHEL, or Scientific Linux ( CentOS, Fedora )
  sudo yum install ansible

To configure the PPA on your machine and install ansible run these commands: ( Ubuntu )

  sudo apt-get install software-properties-common

  sudo apt-add-repository ppa:ansible/ansible

  sudo apt-get update

  sudo apt-get install ansible

======================================================
Adding Hosts to the Hosts File
======================================================
Run the below commands to create and set your ansible Hosts file,

$ echo "127.0.0.1" > ~/ansible_hosts

$ export ANSIBLE_HOSTS=~/ansible_hosts

You can add more hosts to the file in the below format,
  [host groups 1]
    foo.example.com
      bar.example.com

  [host groups 2]
    one.example.com

======================================================
Executing the Role to install Cloudmesh_Client
======================================================

Run the below command,
  ansible-playbook -s client.yml
