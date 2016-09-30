Ansible Role: StandardRole
==========================

[![Build Status](https://travis-ci.org/Aplyca/ansible-role-standardrole.svg?branch=master)](https://travis-ci.org/Aplyca/ansible-role-standardrole)
[![Circle CI](https://circleci.com/gh/Aplyca/ansible-role-standardrole.png?style=badge)](https://circleci.com/gh/Aplyca/ansible-role-standardrole)

Ansible Role for standard creation of roles.

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
  - { role: Aplyca.StandardRole }
```

Role Variables
--------------

See default variables: https://github.com/Aplyca/ansible-role-standardrole/blob/master/defaults/main.yml

Cretae a new role using this as boilerplate
-------------------------------------------

```bash
git clone git@github.com:Aplyca/ansible-role-standardrole.git NewRole;
cd NewRole;
rm -rf .git;
find ./ -type f -exec sed -i '' -e 's/standardrole/newrole/g' {} \;
find ./ -type f -exec sed -i '' -e 's/Standard Role/New Role/g' {} \;
find ./ -type f -exec sed -i '' -e 's/StandardRole/NewRole/g' {} \;
find . -name "standardrole.*" -exec sh -c 'mv "$1" "$(dirname ${1})/newrole."${1##*.}""' _ {} \;
```


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
