# Pi-hole installation on fresh Ubuntu server playbook

## Install dependencies

```bash
ansible-galaxy install -r requirements.yml
```

### Run playbook

Set up the host in /etc/ansible/hosts.yml - make sure to set its `architecture` and `pihole_config_branch` variables to appropriate value.
Available values for `architecture` can be found here: [https://github.com/cloudflare/cloudflared/releases/latest](https://github.com/cloudflare/cloudflared/releases/latest).

Since this playbook sets up a server from scratch (including user creation), it assumes that only the root user exists. 

```bash
ansible-playbook site.yml"
```