### Execute playbook

```bash
ansible-playbook -i inventory.ini install-docker.yaml --ask-become
```

### Generate portainer passwort

```bash
docker run --rm httpd:2.4-alpine htpasswd -nbB admin 'secret' | cut -d ":" -f 2
```

### authentik initial setup

```bash
<authentik_url>/if/flow/initial-setup/
```