anyenv
======

An Ansible role to install anyenv

Requirements
------------

### Update homebrew manually beforehand

You need to update homebrew in advance with the following task.

```
- homebrew: update_homebrew=yes
```

### Restart the shell after running this playbook

The directory specified zsh_custom_dir must be created by running hnakamur.oh-my-zsh.
The zsh config file `anyenv` will be added to the directory.

To load this `anyenv` file, you must run the following command in the shell.

```
exec $SHELL -l
```

Role Variables
--------------

- anyenv_git_url: https://github.com/riywo/anyenv
    - The url of the anyenv git repository.
- anyenv_install_dir: ~/.anyenv
    - The install directory.
- anyenv_rbenv_version: 2.1.2
    - The rbenv version to install. Does not install when empty.
- anyenv_rbenv_global_gems:
    - bundler
    - compass
- anyenv_ndenv_version: v0.10.31
    - The ndenv version to install. Does not install when empty.
- anyenv_ndenv_global_packages:
    - grunt-cli
    - gulp
    - webpack
    - karma-cli

- anyenv_npm_default_license: MIT

Dependencies
------------

- hnakamur.oh-my-zsh

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: hnakamur.anyenv, anyenv_shell_rc_file: ~/.bashrc }

License
-------

MIT
