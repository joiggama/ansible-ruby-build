ruby-build
=========

[![travis](https://img.shields.io/travis/joiggama/ansible-ruby-build/master.svg)](https://travis-ci.org/joiggama/ansible-ruby-build)
[![gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/joiggama/ansible-ruby)

This ansible role aims to install [ruby-build](https://github.com/sstephenson/ruby-build) on ubuntu systems.

Requirements
------------

None.

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
- gather_facts: true
  hosts:        all
  roles:
                - joiggama.ruby-build
```

License
-------

[MIT](LICENSE.md)
