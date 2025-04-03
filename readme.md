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

# Bookstack

**bookstack_app_key** generieren: 

```bash
sudo docker run -it --rm --entrypoint /bin/bash lscr.io/linuxserver/bookstack:latest appkey
```

**Default User:**

**username:** admin@admin.com

**password:** password

## Bookstack and authentik

- https://www.bookstackapp.com/docs/admin/oidc-auth/
- https://docs.goauthentik.io/integrations/services/bookstack/