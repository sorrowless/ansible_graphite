sbog/graphite
=============

Simple role to install graphite

#### Requirements

Ansible 2.4

#### Role Variables

```yaml
graphite:
  docker_labels: []
  # Host directory to store data on
  graphite_storage: /var/graphite/storage

# Docker network-related vars
docker:
  network_name: internal.loc
  network_subnet: 172.22.101.0/24
  network_gateway: 172.22.101.1
  network_iprange: 172.22.101.128/25
```

#### Dependencies

None

#### Example Playbook

```yaml
- name: Install and configure Graphite
  hosts: graphite
  remote_user: root
  roles:
    - { role: graphite, tags: [ 'graphite' ] }
```

#### License

Apache 2.0

#### Author Information

Stanislaw Bogatkin (https://sbog.ru)
