# Pi-hole installation on fresh Ubuntu server playbook

## Install dependencies

```bash
ansible-galaxy install -r requirements.yml
```

### Run playbook

Set up the host in /etc/ansible/hosts.yml - make sure to set its `architecture` variable to appropriate value.
Available values can be found here: https://github.com/cloudflare/cloudflared/releases/latest

```bash
export TAILSCALE_KEY=[auth key]
export PIHOLE_PASSWORD=[pihole password]
ansible-playbook site.yml --extra-vars "target=[target]"
```