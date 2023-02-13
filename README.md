<h1 align="center">ansible-role-dnf-update</h1>

*<p align="center">An Ansible role to apply system updates using the `dnf` package manager.</p>*

## About

Use this Ansible role to apply system updates or 'security only' updates to systems that uses the `dnf` package manager.

This Ansible role:

* Applies the available system updates
* Remove obsolete packages
* Reboot the system

### Status:

[![Actions Status](https://github.com/rossijonas/ansible-role-dnf-update/workflows/CI/badge.svg)](https://github.com/rossijonas/ansible-role-dnf-update/actions)

## Requirements

* Privilege escalation (`sudo`, [learn more](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_privilege_escalation.html#)).

## Role Variables

### `dnfupdate_security_only`

Set the role to apply only updates marked as security updates, instead of 

* **Type**: bool
* **Default**: `false`

  ```
  dnfupdate_security_only: true
  ```

## Dependencies

*(None)*

## Installation

1. Create a `requirements.yml` file at the your project's top level directory and include the following:

  ```
  ---
  - name: dnfupdate
    src: https://github.com/rossijonas/ansible-role-dnf-update
  ```

2. Use `alsible-galaxy` command to fetch dependencies:

  ```
  $ ansible-galaxy install -r requirements.yml
  ```

## Example Playbook

```
---
- hosts: servers
  roles:
    - dnfupdate
```

## License

MIT

## Author Information

GitHub profile: https://github.com/rossijonas

*[-> See more Ansible related repositories from this author](https://github.com/rossijonas?tab=repositories&q=ansible&type=&language=&sort=)*
