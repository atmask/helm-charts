# SMB CSI Driver

The CSI driver to enable provisioning of PVs from SMB share. 

Chart docs: [here](https://github.com/kubernetes-csi/csi-driver-smb/tree/4ab29d8892e7b7a47068046205fa89702bc8da35/charts)

## Installation
```
helm install -n kube-system csi-driver-smb . -f values.yaml
```
