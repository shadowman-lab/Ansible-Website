<!-- This was created with Claude Code -->

hashi_pki_certificate
=====================

An Ansible role for hashi pki certificate.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **hashi_pki_certificate_ttl**: SSL/TLS certificate
  - Default: `47d`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: hashi_pki_certificate
      vars:
        hashi_pki_certificate_ttl: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
