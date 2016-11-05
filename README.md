# Ansible provisioning for app servers on Ubuntu

[![Build Status](https://travis-ci.org/dmishh/ansible-ubuntu-app-server.svg?branch=master)](https://travis-ci.org/dmishh/ansible-ubuntu-app-server)

Easy to use server provisioning for using Ubuntu as an application server for PHP (in progress), Ruby, NodeJS and Elixir (in progress). Tested on Ubuntu 14.04 and Ubuntu 16.04 server editions

**DISCLAIMER – THIS IS UNDER HEAVY DEV, 1.0 RELEASE DATE IS END OF NOV 2016**

## Install

```bash
ansible-galaxy install --roles-path . dmishh.ubuntu-app-server
```

## Roles

### `common` role

Includes installation of a bunch of useful stuff, locale configuration, bash configuration, tmux configuration and creation of a separate user (delpoy_user) for running applications

### `swap` role

Adds swap which persist after machine's restart

### `upgrade` role

Just upgrades all packages in the system

### `security` role

### `nginx` role

### `nodejs` role


## Test with Vagrant

Check `vagrant.yml` for available roles and settings

```bash
vagrant up
```

Sometimes provision failes, you can run it separately with a command: vagrant provision`

## FAQ

### Use with your own roles

TODO

## License

The MIT License. For the full text of license, please, see [LICENSE](/LICENSE)
