#dns_resolvconf:
ansible-playbook -i inventory.yml -e host=all dns_resolvconf.yml --extra-vars "dnsserver=192.168.56.10 dnssuffix=iac.local"

#groups_addmember:
ansible-playbook -i inventory.yml -e host=all groups_addmember.yml  --extra-vars "user=iac group=wheel"

#yum_proxy:
ansible-playbook -i inventory.yml -e host=all yum_proxy.yml  --extra-vars "proxyname=proxy.iac.local proxyport=3128"

#yum_install:
ansible-playbook -i inventory.yml -e host=all yum_install.yml  --extra-vars "yumpackage=telnet"
