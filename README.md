# Ansible Role: Redis

## Description

Apache for all of the webapps I'm deploying.

For the time being, `apache` has become my go-to for deploying small-scale apps. This makes it trivial to deploy a new webserver. The templates contained in here correspond to one or more other roles that I have, or will publish.

## Requirements

* RHEL only

## Role Variables

```yaml
variable: value # comment
```

## Tags

### Role-Specific tags:

* `httpd`
* `httpd_install`
* `httpd_config`

### Global tags:

* `install`
* `config`
* `update`

## Dependencies

* `smacz42.common`
* `smacz42.iptables`

## Example Playbook

```yaml
- name: Roles in Common
  hosts: all
  gather_facts: true
  remote_user: root
  #no_log: true

  roles:
    - { role: common }
    - { role: iptables }
    - { role: httpd }
```

## License

MIT / BSD

## Author Information

This role was created in 2017 by [Andrew Cz](https://andrewcz.com), a student at The Ohio State University.
