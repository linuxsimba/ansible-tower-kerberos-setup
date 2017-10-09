ansible-tower-kerberos-setup
=========

Installs Kerberos dependencies as specified in the [Ansible Tower docs](http://docs.ansible.com/ansible/latest/intro_windows.html#installing-python-kerberos-dependencies)

Requirements
------------

* Ansible 2.3+

Role Variables
--------------

None

Dependencies
------------


* Run this on a Ansible Tower setup server where the Ansible tower setup playbook is installed.

Example Playbook
----------------

```
# install_kerberos.yml
# -------------------

- hosts: tower
  roles:
    - ansible-tower-kerberos-setup
```

Then to execute the playbook from the Tower setup script run `` ansible-playbook -i inventory install_kerberos.yml ``

License
-------

MIT

Author Information
------------------

Stanley at linuxsimba dot com
