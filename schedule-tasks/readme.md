# README

### lastlog.yml
Create a playbook ~/playbooks/lastlog.yml to add a cron job Clear Lastlog on node00 to empty the /var/log/lastlog logs file. The job must run at 12am everyday.


You can use the command echo “” > /var/log/lastlog to empty the lastlog file and schedule should be 0 0 * * *.

## script_cron.yml
We have a script /root/free.sh on node00 that is used to check free system memory. We would like to create a cron Free Memory Check to execute this script at every 2 hour (i.e 12am, 2am, 4am etc), the command to execute the script is sh /root/free.sh and schedule should be 0 */2 * * *.

## reboot.yml
Due to some disk space limitations we want to cleanup /tmp location on node00 host after every reboot. Create a playbook ~/playbooks/reboot.yml to add a cron named cleanup on node00 that will execute after every reboot and will clean /tmp location.

## yum_update.yml
On node00 we want to keep the installed packages up to date, so we would like to run yum updates regularly. Create a playbook ~/playbooks/yum_update.yml and create a cron job as described below:

a. Do not add cron directly using crontab instead create a cron file /etc/cron.d/ansible_yum.

b. The cron must run on every Sunday at 8:05 am.

c. The name of the cron must be yum update.

d. Cron should be added for user root
{Use command yum -y update}
