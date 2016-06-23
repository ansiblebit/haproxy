# Role Name

[![License](https://img.shields.io/badge/license-New%20BSD-blue.svg?style=flat)](https://raw.githubusercontent.com/ansiblebit/haproxy/master/LICENSE)
[![Build Status](https://travis-ci.org/ansiblebit/haproxy.svg?branch=master)](https://travis-ci.org/ansiblebit/haproxy)

[![Platform](http://img.shields.io/badge/platform-ubuntu-dd4814.svg?style=flat)](#)

[![Project Stats](https://www.openhub.net/p/ansiblebit-haproxy/widgets/project_thin_badge.gif)](https://www.openhub.net/p/ansiblebit-haproxy/)

[Ansible][ansible] role to setup [haproxy][haproxy].


## Tests

| Family | Distribution | Version | Test Status |
|:-:|:-:|:-:|:-:|
| Debian | Ubuntu  | Xenial  | [![x86_64](http://img.shields.io/badge/x86_64-passed-006400.svg?style=flat)](#) |
| Debian | Ubuntu  | Trusty  | [![x86_64](http://img.shields.io/badge/x86_64-passed-006400.svg?style=flat)](#) |
| Debian | Ubuntu  | Precise | [![x86_64](http://img.shields.io/badge/x86_64-passed-006400.svg?style=flat)](#) |


## Requirements

- ansible >= 2.0.0


## Role Variables

Unless stated otherwise a default value is provided for
each of the variables mentioned above in the `defaults` directory.


## Dependencies

None.


## Playbooks

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }


## Tags

- **configuration**: configuration tasks.
- **debug**: task to debug role variables.
- **installation**: installation tasks.
- **validation**: task to validate role variables.


## Test

To run the tests you will need to install:

- [tox](https://tox.readthedocs.org/)
- [vagrant](https://www.vagrantup.com/)

To run all tests against all pre-defined OS/distributions * ansible versions:

```
$ tox
```

To run tests for `trusty64`:

```
$ cd tests
$ bash test_idempotence.sh --box trusty64.vagrant.dev
# log file will be stores under tests/log
```

To perform debugging on a specific environment:

```
$ cd tests
$ vagrant up trusty64.vagrant.dev

# to provision using the test.yml playbook (as many time as you need)
$ vagrant provision trusty64.vagrant.dev

# to access the Vagrant box
$ vagrant ssh trusty64.vagrant.dev
```


## Links

- [haproxy][haproxy]
- [ServerLab : Compiling and Running HAProxy from Source on Ubuntu 14](http://www.serverlab.ca/tutorials/linux/network-services/compiling-and-running-haproxy-from-source-on-ubuntu-14/)
- [haproxy init script](https://gist.github.com/serainville)

## License

[BSD][license]


## Author Information

- [steenzout][steenzout]


[ansible]:      https://www.ansible.com         "Ansible"
[license]:      https://github.com/ansiblebit/haproxy/blob/master/LICENSE   "BSD license"
[haproxy]:      http://www.haproxy.org          "haproxy"
[steenzout]:    https://github.com/steenzout/   "Pedro Salgado"

