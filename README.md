ruby-build
=========

[![travis](https://img.shields.io/travis/joiggama/ansible-ruby-build/master.svg)](https://travis-ci.org/joiggama/ansible-ruby-build)
[![gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/joiggama/ansible-ruby)

This ansible role aims to install [ruby-build](https://github.com/sstephenson/ruby-build) on ubuntu systems.

Requirements
------------

All the dependencies are installed by default in the main tasks, if you don't want this role to install them, override the default variable `install_dependencies` to equal `false` when including this role.


Role Variables
--------------

| Name                 | Default                                |                                        |
|:--------------------:|:--------------------------------------:|:--------------------------------------:|
| apt_cache_expiration | 3600                                   | Update apt cache window in seconds     |
| install_dependencies | true                                   | Whether or not to install dependencies |
| root                 | /home/{{ansible_env.USER}}/.ruby-build | Install path for ruby-build            |
| version              | master                                 | Any git reference: branch, tag, commit |

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: all
  roles:
     - role:                 joiggama.ruby-build
       apt_cache_expiration: 3600
       install_dependencies: true
       root:                 ~/.ruby-build
       version:              master
```

License
-------

MIT
