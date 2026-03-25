# Velveta Infra Dev

This repo manages only the Velveta development stack.

Included:
- dev Frappe compose
- dev Next.js compose
- dev-only nginx site config
- dev rebuild flow from GitHub
- runner service templates for the current dev workflows

This repo does not manage production restore or production compose files.

## Inventory

Use:

```bash
/opt/velveta/infra-dev/inventories/dev/hosts.yml
```

The default inventory is local on the current dev VPS.

## Main Commands

Bootstrap:

```bash
cd /opt/velveta/infra-dev
ansible-playbook -i inventories/dev/hosts.yml playbooks/bootstrap.yml
```

Converge:

```bash
cd /opt/velveta/infra-dev
ansible-playbook -i inventories/dev/hosts.yml playbooks/server.yml
```

Rebuild dev:

```bash
cd /opt/velveta/infra-dev
ansible-playbook -i inventories/dev/hosts.yml playbooks/rebuild-dev.yml
```
