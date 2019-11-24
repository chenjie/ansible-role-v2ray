Ansible Role: v2ray
=========

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

Requirements
------------

Ansible

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

This role was created by [Chenjie Ni](https://nichenjie.com)
