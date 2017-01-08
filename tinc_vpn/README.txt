This is simple ansible playbook which installs Tinc mesh vpn client on Ubuntu or Centos operation system.

example:
ansible-playbook -i hosts setup.yml

configuration:
roles/install/defaults/main.yml - default settings for install role
group_vars/all - common setting for all host used by default
group_vars/dev - specific settings for development enviroment
group_vars/stg - specific settings for staging enviroment
group_vars/prod - specific setting for production enviroment

variables:
examples:
roles/install/defaults/main.yml :
	hosts: dev - which hosts group will be used to installation
	user: root - which user will be used to installation and configuration packages on system
	do_upgrade: no - by defatult we are not upgrade system packages possible values are yes,no

group_vars/all :
examples:
	tinc_version: 1.0.30 - wich version of tinc will be installes or compiled from source

group_vars/dev :
examples:
	network_name: dcunderground  - tinc network name 
	tinc_name_host: nuit  - tinc host name
	connect_to_tinc_host: baal - tinc automatic connect to host 
	your_external_ip_or_domain:  example.com - your external IP or domain name
	tinc_allowed_net: 10.0.8.20 - your networks ruted via tinc
