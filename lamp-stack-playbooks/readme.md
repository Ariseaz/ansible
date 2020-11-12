

## ssh key generation for users on db and webserver
Let us setup password less authentication between Ansible Controller and the web and db servers. Create a pair of keys for each user at /home/thor/.ssh/maria and /home/thor/.ssh/john

And distribute the public keys to the web and database servers - lamp-db and lamp-web.


Password for user maria is maria and john is john

--------------------------------------------------------------------
ssh-keygen -f /home/thor/.ssh/maria 
ssh-keygen -f /home/thor/.ssh/john
ssh-copy-id -i /home/thor/.ssh/maria maria@lamp-db
ssh-copy-id -i /home/thor/.ssh/john john@lamp-web



---------------------------------------------------------------------