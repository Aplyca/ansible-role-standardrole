Ansible Role: StandardRole
==========================

Ansible Role that describes instances and add them to hosts group in order to be used in others playbooks.

Requirements
------------

Use hash behavior for variables in ansible.cfg
See example: https://github.com/Aplyca/ansible-role-standardrole/blob/master/tests/ansible.cfg
See official docs: http://docs.ansible.com/intro_configuration.html#hash-behaviour

Installation
------------

Using ansible galaxy:
```bash
ansible-galaxy install Aplyca.StandardRole
```
You can add this role as a dependency for other roles, add the role to the meta/main.yml file of your own role:
```yaml
dependencies:
  - { role: Aplyca.EC2Describe }
```

Role Variables
--------------

See default variables: https://github.com/Aplyca/ansible-role-ec2describe/blob/master/defaults/main.yml

Dependencies
------------

None.

Testing
-------
Using Vagrant:

```bash
tests/vagrant.sh
```
Using Docker:

```bash
tests/docker.sh
```

License
-------

MIT / BSD

Author Information
------------------

Mauricio Sánchez from Aplyca SAS (http://www.aplyca.com)
