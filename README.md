Ansible Role: atom
==================

This role ensures that configured packages for Atom are installed.


Requirements
------------

* Atom and Atom Package Manager (APM)


Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
atom_upgrade_all: False
```

Whether to upgrade all Atom packages installed. If you prefer to manually update packages via `apm` command or in Atom, leave this set to `False`.

```
atom_packages:
  - language-ansible
```

Packages you would like to make sure are installed via `apm install`.


Dependencies
------------

* jgkim.cask


Example Playbook
-------------------------

```
- hosts: localhost
  connection: local
  vars:
    atom_upgrade_all: True
    atom_packages:
      - language-ansible
  roles:
     - { role: jgkim.atom }
```


License
-------

GPLv3


Author Information
------------------

This role was written by [James G. Kim](http://jayg.org/), based on Homebrew Cask Ansible module by [Daniel Jaouen](http://il.luminat.us/).
