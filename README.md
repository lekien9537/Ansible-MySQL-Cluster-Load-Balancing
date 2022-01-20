Building a simple scalable Database systems using Ansible Playbooks
-------------------------------------------

These playbooks use Ansible 2.12.1 and jinja version = 2.10.1.

Ansible playbook that install Mysql-Cluster 8.x.x (Archived Versions) for Ubuntu x86_64.

More detail these versions here: https://downloads.mysql.com/archives/cluster/.

Overview
-------------------------------------------

MySQL Cluster +  Load Balancing: Harpxy + Keepalived

<p align="center">
  <img src="overview" width="75%"/>
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
