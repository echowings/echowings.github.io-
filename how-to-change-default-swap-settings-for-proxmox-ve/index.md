# How to Change Default Swap Settings for Proxmox Ve


# How to change default swap settings for Proxmox VE


 - Check Default swap policy from value 60 to 0

 ``` bash
 cat /proc/sys/vm/swappiness
 #default value is 60 , it means when the memory remain 60, the swap will be enable
 
 ```
 
 - Change swap policy

 
 ``` bash
 # Temp to change default swap enable when memory remain 0.
 sysctl vm.swappiness=0
 
 # Permanent to change swapp
 cat << EOF >> /etc/sysctl.conf
 vm.swappiness=0
 
 #apply settings
 sysctl -p
 
 
 # check 
  cat /proc/sys/vm/swappiness
 ```
 
- Vacuum swap 

 ``` bash
swapoff -a
swapon -a
```




