# Some_tips_for_management_promxmoxve


# Some tips for management proxmxo VE



## Force shutdown a vm

```bash
#List all vm in pve
qm list 

# qm unlock the specific vm
qm unlock <vmid>

# qm stop the specific vm
qm stop <vmid>

# qm shutdown the specific vm
qm shutdown <vmid>


# Check vm status
qm list | grep <vmid>
```
