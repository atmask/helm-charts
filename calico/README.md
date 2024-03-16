# Calico
This chart configures the tigera-operator for deploying Calico CNI into my cluster. The CNI uses VXLAN as an overlay network for communication in the cluster. There is one ippool (10.0.0.0/24) with 255 ips. This is plenty for my small cluster. The IPAM block size is /28, meaning there are 16 ips per block

# Installation

First, create the `tigera-operator` namespace and then install the chart:
```
>>> kubectl create ns tigera-operator
namespace/tigera-operator created

>>> helm install calico . -n tigera-operator -f values.yaml
```