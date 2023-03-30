Install libvirt and qemu-kvm on your system:

```
sudo dnf install libvirt qemu-kvm
```

Add yourself to the libvirt group:
```
sudo usermod -a -G libvirt $(whoami)
```

Update your current session to apply the group change:
```
newgrp libvirt
```

Install podman
```
yum install podman -y
```

Install the KVM driver binary and make it executable as follows:
```
sudo curl -L https://github.com/dhiltgen/docker-machine-kvm/releases/download/v0.10.0/docker-machine-driver-kvm-ubuntu16.04 -o /usr/local/bin/docker-machine-driver-kvm
```

Minishift installation
```
wget https://github.com/minishift/minishift/releases/download/v1.34.0/minishift-1.34.0-linux-amd64.tgz

tar xzf minishift-1.34.0-linux-amd64.tgz

sudo cp minishift-1.34.0-linux-amd64/minishift /usr/local/bin

sudo chmod +x /usr/local/bin/minishift
```

Start Minishift
```
minishift start
```

Delete minishift
```
minishift delete --clear-cache

minishift delete --clear-cache

```

Create environment
```
minishift oc-env

export PATH="/root/.minishift/cache/oc/v3.11.0/linux:$PATH"
```