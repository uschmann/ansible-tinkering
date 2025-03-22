### Execute playbook

```bash
ansible-playbook -i inventory.ini install-docker.yaml --ask-become
```

### Generate portainer passwort

```bash
docker run --rm httpd:2.4-alpine htpasswd -nbB admin 'secret' | cut -d ":" -f 2
```