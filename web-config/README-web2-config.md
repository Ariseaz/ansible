We have a playbook ~/playbooks/web2-config.yml, it has some existing code to change apache’s default port 80 to port 8082 as we want to run Apache on port 8082 on web2 node. Make some changes as given below before running the playbook.


A. Add an entry in ~/playbooks/inventory for web2 node, IP address of web2 node is 172.20.1.101 and ssh password and username are same as of web1.

B. Update web2-config.yml to install httpd before updating its port in config, also start/enable its service.

C. Install firewalld package and start/enable its service.

D. As now Apache will listen on port 8082 so edit the playbook to add firewall rule in public zone so that Apache can allow all incoming traffic.

inventory file setup
web1 ansible_host=172.20.1.100 ansible_ssh_pass=Passw0rd ansible_user=root
web2 ansible_host=172.20.1.101 ansible_ssh_pass=Passw0rd ansible_user=root