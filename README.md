## Kafka Ansible Role

[![Build Status](https://travis-ci.org/bilalcaliskan/remi-ansible-role.svg?branch=master)](https://travis-ci.org/bilalcaliskan/remi-ansible-role)

Sets up Remi repository on RHEL/CentOS 7/8 servers.

## Requirements

No special requirements; note that this role requires root access, so either run it in a playbook with a global `become: yes`, or invoke the role in your playbook like:

      - hosts: all
        roles:
          - role: bilalcaliskan.remi
            become: true

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

        repo_url: http://fr2.rpmfind.net/linux/remi/enterprise/$releasever/remi/$basearch/
        public_key_url: https://rpms.remirepo.net/RPM-GPG-KEY-remi

## Dependencies

None

## Example Playbook File

    - hosts: all
      become: true
      roles:
        - role: bilalcaliskan.remi
          vars:
            empty_var: true

* Inside `vars/main.yml`*:

    kafka_version: 123.123

## License

MIT / BSD
