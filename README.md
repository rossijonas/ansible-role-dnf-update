<h1 align="center">ansible-role-dnf-update</h1>

*<p align="center">An Ansible role to apply system updates using the `dnf` package manager.</p>*

## About

Use this Ansible role to apply system updates or 'security only' updates to systems using the `dnf` package manager.

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

Set the role to only apply updates marked as security updates.

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

2. Use `ansible-galaxy` command to fetch dependencies:

  ```
  $ ansible-galaxy install -r requirements.yml
  ```

## Example Playbooks

* Apply all updates available:

```
---
- hosts: servers
  roles:
    - dnfupdate
```

* Apply security updates only:

```
---
- hosts: servers
  roles:
    - role: dnfupdate
      vars: 
        dnfupdate_security_only: true
```

## License

MIT

## Author Information

GitHub profile: https://github.com/rossijonas

*[-> See more Ansible related repositories from this author](https://github.com/rossijonas?tab=repositories&q=ansible&type=&language=&sort=)*
