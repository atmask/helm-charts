# SMB CSI Driver

The CSI driver to enable provisioning of PVs from SMB share. 

Chart docs: [here](https://github.com/kubernetes-csi/csi-driver-smb/tree/4ab29d8892e7b7a47068046205fa89702bc8da35/charts)

## Installation
```
helm install -n kube-system csi-driver-smb . -f values.yaml
```


## SMB Creds
This chart will not populate any secrets in the cluster w/ smb connection creds. These are, at this time, manually created using:
```
kubectl create secret generic smbcreds --from-literal username="USERNAME" --from-literal password="PASSWORD"
```