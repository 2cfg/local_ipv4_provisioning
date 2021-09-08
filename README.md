# local_ipv4_provisioning
Local IPv4 provisioning for ISP Manager node

Add to /etc/rc.local: 
```
bash /etc/rc.local.d/*
``` 

Add every minutes cronjob:
```
* * * * * cd /root/ansible-control/ && /usr/local/bin/ansible-playbook ./ipaddr_provisioning.yml > /root/cron_log 2>&1
```
