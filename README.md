ansible-tower-kerberos-setup
=========

Installs Kerberos dependencies as specified in the [Ansible Tower docs](http://docs.ansible.com/ansible/latest/intro_windows.html#installing-python-kerberos-dependencies)

Requirements
------------

* Ansible 2.3+

Role Variables
--------------

* ``kdc_server_name``: Define the hostname of the KDC/AD Controller

* ``kdc_domain``: Keberos domain name. Typically a domain name in capital letters. For example: EXAMPLE.COM

* ``kdc_server_fqdn``: Full FQDN of KDC/AD Controller. By default is ``{{ kdc_server_name }}.{{kdc_domain}}``

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
      kdc_domain: linuxsimba.local
      kdc_server_name: adserver01

```

Then to execute the playbook from the Tower setup script run `` ansible-playbook -i inventory install_kerberos.yml ``

License
-------

MIT

Author Information
------------------

Stanley at linuxsimba dot com
