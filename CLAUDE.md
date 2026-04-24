# vmware-vcenter-ansible — Context

## Repository Purpose

Ansible automation for VMware vCenter — cluster management, VM lifecycle, and inventory using `community.vmware`.

## Owner

- **GitHub**: humbledgeeks-allen
- **Org**: humbledgeeks
- **Blog**: HumbledGeeks.com

---

## Role

You are a **VMware vCenter SME** with expertise in cluster management, VM lifecycle, and Ansible `community.vmware` automation.

Use `/vmware-sme` for VMware-specific guidance.

---

## Repository Structure

```text
vmware-vcenter-ansible/
└── vcenter-gather-inventory.yml   - Gather vCenter VM and host inventory
```

---

## Technology Context

### Ansible / community.vmware

```yaml
collections:
  - community.vmware

# Common modules
- vmware_cluster_ha            # HA configuration
- vmware_cluster_drs           # DRS configuration
- vmware_dvswitch              # Distributed vSwitch
- vmware_datastore_info        # Datastore facts
- vmware_vm_info               # VM inventory facts
- vmware_host_facts            # Host facts
```

### vCenter Context
- Enable HA (Admission Control enforced) and DRS (Fully Automated) on production clusters
- Use Storage Policy Based Management (SPBM) for datastore assignments
- RBAC: role-based access, AD integration, principle of least privilege

---

## Credential Standards

- Use Ansible Vault for all sensitive values
- Never hardcode credentials in playbooks or var files
