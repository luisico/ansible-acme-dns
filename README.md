# Ansible Role for acme.sh

Install acme.sh and issue certificate with DNS challenge.

#### Example Playbook

Requires `root` if not using `become` by default.

```
- hosts: server
  roles:
    - role: acme
      become: yes
      become_user: root
```

#### Example Variables

```
acme_dns_api: 'infoblox'
acme_domain: 'my.domain.example'

acme_infoblox_host: 'infoblox.host.example'
acme_infoblox_user: '{{ vault_acme_infoblox_user }}'
acme_infoblox_pass: '{{ vault_acme_infoblox_pass }}'
acme_infoblox_view: 'my_infobox_view'

acme_path_cert: '/path/to/cert/file'
acme_path_fullchain: '/path/to/fullchain/cert/file'
acme_path_key: 'path/to/key/file'
```
