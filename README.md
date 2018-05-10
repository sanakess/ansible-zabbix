Zabbix agent template
=========

Install zabbix-agent and init.d script

Requirements
------------
Centos 7

Debian 8-9

Role Variables
--------------
./group_vars/all
```
#uninstall zabbix-agent. Defaukt to "false". Set to "true" if you want to delete zabbix-agent
uninstall_zabbix_agent: false

#zabbix_checks_active. Default to "true". Set to "false" if you want to set passive checks
zabbix_checks_active: true
```

Example Playbook
----------------

```
- hosts: zabbix-clients
  become: yes
  roles:
  - zabbix_agent
  - zabbix_agent_systemd
```

License
-------


Author Information
------------------
sanakess