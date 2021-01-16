## Kafka Ansible Role

[![CI](https://github.com/bilalcaliskan/remi-ansible-role/workflows/CI/badge.svg?event=push)](https://github.com/bilalcaliskan/remi-ansible-role/actions?query=workflow%3ACI)

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

        repo_url: http://fr2.rpmfind.net/linux/remi/enterprise/$releasever/remi/$basearch/
        public_key_url: https://rpms.remirepo.net/RPM-GPG-KEY-remi

## License

MIT / BSD
