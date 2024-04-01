# NextCloud role for Ansible

## Variables

```yaml
nextcloud:
  version: 21
  domain: cloud.example.com
  trusted_domains: 192.168.*.* cloud.example.com
  internal_port: 4000
  admin:
    user: admin
    password: adminpass
  nginx: # only affects how server config generation
    includes:
      - snippets/acme-challenge.conf
  mounts:
    - /mnt/hdd
```

External handler "Restart Nginx" is used. Provided by https://github.com/n1k0r/ansible-role-nginx
