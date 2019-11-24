Ansible Role: v2ray
=========

[![Build Status](https://travis-ci.com/jellycsc/ansible-role-v2ray.svg?branch=master)](https://travis-ci.com/jellycsc/ansible-role-v2ray)

An Ansible Role that installs V2Ray proxy on RHEL/CentOS, Debian/Ubuntu and Arch Linux.

Default Configs
---------------

| Key | Value |
|---|---|
| Server IP | `<your_server_ip>`  |
| Protocol | `Vmess` |
| Port | `50000` |
| UUID | `b831381d-6324-4d53-ad4f-8cda48b30811` |
| AlterId | `4` |
| Encryption | `auto` |

Tested Platforms
------------

- Red Hat UBI 8
- CentOS 7
- CentOS 8
- Ubuntu 16.04
- Ubuntu 18.04
- Debian 8
- Debian 9
- Debian 10

Role Variables
--------------

You can set your custom `config.json` path:

    config_json_path: "path/to/config.json"

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: proxy_servers
      become: yes
      vars_files:
        - vars/main.yml
      roles:
         - { role: jellycsc.v2ray }


License
-------

[MIT](LICENSE)

Author Information
------------------

This role was created by [Chenjie Ni](https://nichenjie.com).
