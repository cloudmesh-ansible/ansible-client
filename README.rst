======================================================
A Simple Ansible Role for Installing Cloudmesh_Client
======================================================

This ansible role will install cloudmesh_client in the hosts specified in the hosts file

======================================================
Installing Ansible in your local System
======================================================

Best is to use virtualenv to not effect your locally deployed system with python
How to do that can be found for example in the cloudmesh_client documentation at:

* http://cloudmesh.github.io/client/system.html

YOu should only update your system and not install cloudmesh_client from the instructions above, as this ansible role will install cloudmesh client for you. We assume you have pip installed and updated with::
  
  $ pip install pip -U
  $ pip install ansible

In some system you get a pre-packaged environment for ansible, use those if you have sufficient access to the operating system. For example on CentOS, RHEL, or Scientific Linux ( CentOS, Fedora ) you can use::

  $ sudo yum install ansible

To configure the PPA on your machine and install ansible run these commands: ( Ubuntu )::

  $ sudo apt-get install software-properties-common
  $ sudo apt-add-repository ppa:ansible/ansible
  $ sudo apt-get update
  $ sudo apt-get install ansible

Make sure that python is of at least version 2.7 (but not 3)
and pip is up to date to the newest version.

======================================================
Adding Hosts to the Hosts File
======================================================
Run the below commands to create and set your ansible Hosts file::

  $ echo "127.0.0.1" > ~/ansible_hosts
  $ export ANSIBLE_HOSTS=~/ansible_hosts


You can add more hosts to the file in the below format::

  [host groups 1]
  foo.example.com
  bar.example.com

  [host groups 2]
  one.example.com

======================================================
Executing the Role to install Cloudmesh_Client
======================================================

Now you can install cloudmesh on the specified hosts with the command::

  $ ansible-playbook -s client.yml
  
