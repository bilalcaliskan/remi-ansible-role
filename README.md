## Remi Ansible Role

[![CI](https://github.com/bilalcaliskan/remi-ansible-role/workflows/CI/badge.svg?event=push)](https://github.com/bilalcaliskan/remi-ansible-role/actions?query=workflow%3ACI)

Sets up Remi repository on RHEL/CentOS 7/8 servers.

### Requirements

This role requires minimum Ansible version 2.4 and maximum Ansible version 2.9. You can install suggested version with pip:
```
$ pip install "ansible==2.9.16"
```

No special requirements. Also note that this role requires root access, so either run
it in a playbook with a global `become: true`, or invoke the role in your playbook like:

```yaml
- hosts: all
  become: true
  roles:
    - bilalcaliskan.remi
```

### Role Variables
See the default values in [defaults/main.yml](defaults/main.yml). You can overwrite them in [vars/main.yml](vars/main.yml) if neccessary or you can set them while running playbook.

### Dependencies

None

### Example Playbook File

```yaml
- hosts: all
  become: true
  roles:
    - role: bilalcaliskan.remi
      vars:
        repo_url: http://fr2.rpmfind.net/linux/remi/enterprise/$releasever/remi/$basearch/
        public_key_url: https://rpms.remirepo.net/RPM-GPG-KEY-remi
```

### License

MIT / BSD
