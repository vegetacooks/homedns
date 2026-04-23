 ## Kernel tuning for Redis on Pi

 Redis requires these kernel settings to run optimally.

These settings should be setup when you first get started so that Redis and Unbound behave as expected.

### Apply immediately
```
sudo sysctl vm.overcommit_memory=1
sudo sysctl -w net.core.wmem_max=8388608
sudo sysctl -w net.core.rmem_max=8388608
```

### Edit to host machine sysctl.conf to persist
`sudo nano /etc/sysctl.conf `
```
vm.overcommit_memory=1
net.core.rmem_max=8388608
net.core.wmem_max=8388608
```
