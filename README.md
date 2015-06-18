common
=========

This role is used to perform common tasks which is needed to set up any new server 
- Configure rkhunter to report any changes on the system
- Add the admins team to the new server, and give them full access
- Install common packages needed
- Disable IPv6
- Set locale
- Set time zone
- Adjust some common comfiguration for vim, histroy, and screen commands  
Requirements
------------
The Common role requires a Debian based Linux host and is tested to function on Ubuntu with the following specific software versions:

Ansible: 1.8.2
Ubuntu: 14.04

Role Variables
--------------

All variables are specified in defaults/main.yml

variable name : admins 
default value : list contain users ( admin1, admin2, admin3 ) 
description: add name and public key file of a user to be created on the server

variable name : timezone
default value : "UTC"
description: set your timezone 

variable name : admin_mail
default value : admin@example.com
description : add admin email which is used to receive rkhunter warning 

Dependencies
------------

NONE

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: spirula.common, tags: ["common"] }

License
-------

MIT

Author Information
------------------

This role was created by the admins team in spirula systems company

company website: http://www.spirulasystems.com/

