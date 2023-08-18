joenyland.sanoid
=========================

[![CI](https://github.com/JoeNyland/ansible-sanoid-role/actions/workflows/ci.yml/badge.svg)](https://github.com/JoeNyland/ansible-sanoid-role/actions/workflows/ci.yml)

Installs and configures Sanoid.

Requirements
------------

None.

Role Variables
--------------

### `sanoid_templates`

A hash of templates.

### `sanoid_policies`

A hash of policies.

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: server
  roles:
    - role: sanoid
      vars:
        sanoid_templates:
          tank:
            autosnap: 'yes'
            autoprune: 'yes'
            frequently: 0
            hourly: 0
            daily: 30
            monthly: 3
            yearly: 0
        sanoid_policies:
          tank:
            use_template: tank
            recursive: 'yes'


```

License
-------

MIT

Author Information
------------------

⌨️ with ❤️ by [Joe Nyland](https://joe.nyland.io)
