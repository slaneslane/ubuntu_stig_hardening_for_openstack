# Budowanie:
```bash
packer init .
packer build packer-template.json
```

### output to:
output-ubuntu-22.04-hardened-stig/ubuntu-22.04-hardened-stig.qcow2

## ładowanie do Glance
```bash
openstack image create "Ubuntu 22.04 Hardened STIG" \
  --file output-ubuntu-22.04-hardened-stig/ubuntu-22.04-hardened-stig.qcow2 \
  --disk-format qcow2 --container-format bare --public
```
