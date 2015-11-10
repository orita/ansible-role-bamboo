Ansible Role:bamboo
=========

Install atlassian bamboo for RedHat/CentOS.

[Running Bamboo as a Linux service - Atlassian Documentation](https://confluence.atlassian.com/bamboo/running-bamboo-as-a-linux-service-416056046.html)

Requirements
------------

None.

Role Variables
--------------

```
bamboo_binary_url: https://www.atlassian.com/software/bamboo/downloads/binary/atlassian-bamboo-5.9.7.tar.gz
bamboo_basedir: /opt/atlassian/bamboo
bamboo_homedir: /var/atlassian/application-data/bamboo
```

Dependencies
------------
- ericmdev.libselinux-python
- geerlingguy.java

Example Playbook
----------------

```
- hosts: all
  vars:
    java_packages:
      - java-1.8.0-openjdk
  roles:
    - ericmdev.libselinux-python
    - geerlingguy.java
    - orita.bamboo
```

License
-------

BSD

Author Information
------------------
