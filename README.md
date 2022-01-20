Building a simple scalable Database systems: MySQL Cluster +  Load Balancing using Ansible Playbooks.
-------------------------------------------

These playbooks require Ansible 1.2.

Ansible playbook that install Mysql-Cluster 8.x.x (Archived Versions) for Ubuntu x86_64 (more detail these versions here: https://downloads.mysql.com/archives/cluster/)

Overview
-------------------------------------------

<p align="center">
  <img src="overview.jpg" width="45%"/>
</p>

Adding nodes
-------------------------------------------

Just modify/add your nodes in these sections:

    [ManagementNodes]
    192.168.1.111
    192.168.1.112

    [DataNodes]
    192.168.1.113
    192.168.1.114

    [SQLNodes]
    192.168.1.111
    192.168.1.112

    [LoadBalancer]
    192.168.1.115
    192.168.1.116


Installation
-------------------------------------------

    ansible-playbook -i hosts mysql_cluster.yml