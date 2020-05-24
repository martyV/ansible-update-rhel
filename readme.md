# Update RHEL with latest updates

A simple playbook to update your RHEL7/CentOS7 environment.

## Inventory
The inventory file is structured around a couple of groups, the reason for this is to have a bit more control when upgrading many OS installations. So group your hosts as you prefer depending on the amount of hosts to be upgraded.

## Playbook
The playbook consist of two main parts, update of the packages and then reboot. These two main parts are tagged with tags named `pkg` and `reboot`. 
Remember that it can take a long time to update a lot of packages so have patience.

## Examples
To run the full playbook
```
ansible-playbook main.yml
```
To run the playbook on a specific host
```
ansible-playbook -l host1 main.yml
```
To run the playbook on the grp1 hosts
```
ansible-playbook -l grp1 main.yml
```
To run the playbook on the hosts in grp2 with no reboot
```
ansible-playbook -l grp2 main.yml --skip-tags reboot
```
