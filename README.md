# NSO-project

NSO project aims to automate the deployment and configuration of a network infrastructure using OpenStack and Ansible. It provides a set of programs and scripts to streamline the setup process.

*Install

The INSTALL script is responsible for automating the deployment process. It performs the following tasks: Loads environment variables from the openRC file for authentication. Creates the required network infrastructure in OpenStack if it doesn't exist. Creates a key pair for SSH access if it doesn't exist. Creates a security group and adds the necessary rules for network access. Creates and configures the servers using OpenStack APIs, including attaching floating IPs. Generates an SSH config file and a hosts file for Ansible. Executes an Ansible playbook for further configuration and provisioning of the network infrastructure. Ansible Playbook aims to automate the deployment and configuration of a Flask application on multiple nodes, configure HAproxy load balancer and SNMP monitoring, and set up monitoring tools such as Prometheus and Grafana on a Bastion host, while node exporter on all the webservers and proxy nodes. The script utilizes various openstack commands, installation of jq to perform necessary operations.

*Operate

Operate program automates the deployment and management of a set of nodes in an OpenStack environment. It utilizes the OpenStack command-line tools and Ansible playbook for server creation, configuration, and deployment. The program reads a configuration file, server.conf, to determine the required number of nodes and checks the existing nodes in the environment. If the required number of nodes is not met, the program creates new nodes, fetches their IP addresses, and updates the hosts and SSH config files. It then runs an Ansible playbook to deploy the required services on the nodes. Finally, it validates the operation by accessing the nodes' IP addresses and prints the response content.

*Cleanup

Cleanup program cleans up resources created by the operate and install programs in an OpenStack environment. It deletes the nodes, servers, subnets, networks, routers, key pairs, security groups, and volumes associated with the specified project. The program uses the OpenStack command-line tools to perform the cleanup tasks and prints the status of the remaining resources after the cleanup process is completed.


Requirements:
Ubuntu-20.04 LTS, openstack-5.2.0, jq-1.6, python-3.8.10
