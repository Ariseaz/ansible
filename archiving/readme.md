Create an inventory file under ~/playbooks directory on Ansible controller host and add web1 as managed node. IP address of web1 node is 172.20.1.100, SSH user is root and password is Passw0rd.


Create a playbook ~/playbooks/zip.yml to make a zip archive opt.zip of /opt directory on web1 node and save it under /root on web1 node itself.

On Ansible controller we have a zip archive local.zip. We want to extract its contents on web1 under /tmp directory. Create a playbook local.yml under ~/playbooks to complete the task.

On web1 node we have an archive data.tar.gz under /root directory, extract it under /srv directory by developing a playbook ~/playbooks/data.yml and make sure data.tar.gz archive is removed after that.

We have three files on web1 node /root/file1.txt, /usr/local/share/file2.txt and /var/log/lastlog. Create a bz2 archive of all these files and save it under /root, name the archive as files.tar.bz2. You can create ~/playbooks/files.yml playbook for it.

## Project
### nginx.yml
We want to setup nginx on web1 node with some sample html code. Create a playbook ~/playbooks/nginx.yml to do so. Below are the details about the task:


a. Install nginx package and start/enable its service.

b. Extract /root/nginx.zip archive under /usr/share/nginx/html directory.

c. Inside /usr/share/nginx/html/index.html replace line This is sample html code with line This is KodeKloud Ansible lab.


