# Ansible role for PhantomJS

[![Build Status](https://travis-ci.org/torian/ansible-role-phantomjs.svg)](https://travis-ci.org/torian/ansible-role-phantomjs)

Ansible role to build [PhantomJS](http://phantomjs.org/).

## Defaults

```
phantomjs_version:  2.0.0
```

## Usage

```
---
- hosts: all

  vars:
    - phantomjs_version: 1.9.1

  roles:
    - { role: torian.phantomjs }

```

