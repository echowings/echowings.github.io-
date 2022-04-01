# How to Rename Vm Id on Pve


# How to rename VMID on PVE
```bash
VMID=121 && \ 
	NEW_VMID=1001 && \
	POOL_NAME=tank && \
	qm unlock $VMID && \
	qm stop $VMID && \
	sed -i "s/$VMID/$NEW_VMID/g" /etc/pve/qemu-server/$VMID.conf && \
	mv /etc/pve/qemu-server/$VMID.conf /etc/pve/qemu-server/$NEW_VMID.conf &&  \
	rbd --pool $POOL_NAME rename vm-$VMID-disk-0 vm-$NEW_VMID-disk-0 &&\
 	qm start $NEW_VMID
```
