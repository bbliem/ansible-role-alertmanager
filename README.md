# ansible-role-alertmanager

Ansible role for installing Prometheus Alertmanager

## Variables

### General

- `alertmanager_docker_image` [default: `prom/alertmanager:v0.21.0`]
- `alertmanager_matrix_docker_image` [default: `jaywink/matrix-alertmanager:v0.5.0`]
- `alertmanager_config_dir` [default: `/usr/local/etc/alertmanager`]
- `alertmanager_hostname` [required]
- `alertmanager_web_external_url` [default: `https://{{ alertmanager_hostname }}`]
- `alertmanager_traefik_router_rule` [default: `Host(``{{ alertmanager_hostname }}``)`]
- `alertmanager_basic_auth` [required]

### Matrix notifications

- `alertmanager_matrix_alertmanager_secret` [required]
- `alertmanager_matrix_homeserver_url` [required]
- `alertmanager_matrix_user` [required]
- `alertmanager_matrix_alertmanager_token` [required]
- `alertmanager_matrix_alertmanager_rooms` [required]
