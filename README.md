# Ansible role for PhantomJS

[![Build Status](https://travis-ci.org/torian/ansible-role-phantomjs.svg)](https://travis-ci.org/torian/ansible-role-phantomjs)

Ansible role to build [PhantomJS](http://phantomjs.org/) from source.

*NOTE*: Building phantomJS from source takes a bit (long bit actually).

## Supported Platforms

  * Ubuntu trusty
  * Centos 6
  * Amazon Linux 2015.09
  * Amazon Linux 2015.03

## Defaults

```
phantomjs_version:  2.0.0
phantomjs_build_jobs: 4
phantomjs_bin: /usr/local/bin/phantomjs
```

## Usage

The role will clone the git repo, using the specified tag / branch through
`phantomjs_version` var, and will install it in `phantomjs_bin`.

To install a version other than the default one:

```
---
- hosts: all

  vars:
    - phantomjs_version: 1.9.1

  roles:
    - { role: torian.phantomjs }

```

If the version needs to be changed (downgraded or upgraded) the
`phantomjs_force_build` needs to be set to `true`, preferably
through an `extra_var`:

```
---
- hosts: all

  vars:
    - phantomjs_version:     1.9.8
    - phantomjs_force_build: true

  roles:
    - { role: torian.phantomjs }

```


