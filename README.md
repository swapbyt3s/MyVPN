# MyVPN

## Requirements:

```
brew install terraform
brew install ansible
```

## Create instance

```
export SCALEWAY_ORGANIZATION=<your-organization-key>
export SCALEWAY_TOKEN=<your-token>

terraform init
terraform apply
```

## Configure

```
ansible -m ping --inventory=hosts myvpn
ansible-playbook --inventory=hosts ansible.yml
```

### Test DNSCrypt

Check with [URL](https://www.dnsleaktest.com/) and extend test, compare both result without VPN and with VPN, the good news is when you have many and different servers with the same protocol.
