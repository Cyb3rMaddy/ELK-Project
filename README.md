## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.
![Azure VM Topology](https://user-images.githubusercontent.com/61891953/169565344-9e34df08-6bcc-4ed1-abda-8ade9e5035f4.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the playbook file may be used to install only certain pieces of it, such as Filebeat

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build

### Description of the Topology
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting access to the network.

A jumpbox or bastion server serves as a gatway to gain entry into a remote network. Many times the primary mode of access is ssh and without the key access is forbidden
A loadbalancer is meant to serve as a specific point of access for a service that is served by multiple machines. This allows high availability models to function properly
Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the log files and system resources.

Filebeat is meant primarily to watch for system logs and forward any changes to the Elasticsearch Host
Metricbeat is used only for gathering metrics and system resources usage for display in Elasticsearch
The configuration details of each machine may be found below.

Name	Function	IP Address	Operating System
JumpBox	Gateway	10.0.0.4	Ubuntu
Web1	Web Server	10.0.0.5	Ubuntu
Web2	Web Server	10.0.0.6	Ubuntu
ELK	ElasticSearch Stack	10.1.0.4	Ubuntu

### Access Policies
