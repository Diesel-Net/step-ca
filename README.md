[![Build Status](https://drone.kiwi-labs.net/api/badges/Diesel-Net/step-ca/status.svg)](https://drone.kiwi-labs.net/Diesel-Net/step-ca)

# step-ca
Private (internal) ACME-based Certificate Authority on docker swarm. Using [Smallstep's step-ca](https://smallstep.com/docs/step-ca).

## Dependencies
- Ansible 2.11+

## Installing Dependencies
```bash
ansible-galaxy install -r .ansible/roles/requirements.yaml -p .ansible/roles --force
```

## Deploy
Right now each environment is defined as an independent Virtual Machine (single-node swarm leaders)
```bash
ansible-playbook .ansible/deploy.yaml -i .ansible/inventories/production/hosts --vault-id ~/.tokens/master_id
```
