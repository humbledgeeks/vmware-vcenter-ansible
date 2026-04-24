# Contributing to vmware-vcenter-ansible

## Requirements

- Ansible 2.12+
- VMware collection: `ansible-galaxy collection install community.vmware`
- ansible-lint: `pip install ansible-lint`

## Playbook Header

All playbooks must include a comment block:

```yaml
---
# playbook-name.yml
# Author  : HumbledGeeks / Allen Johnson
# Date    : YYYY-MM-DD
# Version : 1.0
# Module  : community.vmware
# Repo    : vmware-vcenter-ansible
#
# Description: Brief description
```

## Credential Standards

- Use Ansible Vault for all sensitive values
- Never hardcode credentials in playbooks or var files

## Linting

```bash
ansible-lint .
```

## Pull Request Checklist

- [ ] Playbook header present with all fields
- [ ] No hardcoded credentials
- [ ] ansible-lint passes with no errors
- [ ] README updated if new playbooks added
