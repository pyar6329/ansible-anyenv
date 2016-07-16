anyenv
======

[![Build Status](https://travis-ci.org/pyar6329/ansible-anyenv.svg?branch=master)](https://travis-ci.org/pyar6329/ansible-anyenv)

An Ansible role to install anyenv

Requirements
------------

Restart the shell after running this playbook

Role Variables
--------------

- anyenv.git_url: https://github.com/riywo/anyenv
    - The url of the anyenv git repository.
- anyenv.install_dir: ~/.anyenv
    - The install directory.

- rbenv.version: 2.3.1
    - The rbenv version to install. Does not install when empty.
- rbenv.global_packages:
    - bundler

- ndenv.version: v6.3.0
    - The ndenv version to install. Does not install when empty.
- ndenv.global_packages: []

- npm_default_license: MIT

- pyenv.version: 3.5.2
    - The pyenv version to install. Does not install when empty.
- pyenv.global_packages:
    - pip-tools
    - neovim

Dependencies
------------

- None

Example Playbook
----------------

    - hosts: localhost
      roles:
         - { role: pyar6329.anyenv }

License
-------

MIT
