```bash
edgeProxy:
  enable: true
  
because of this microservice is able to open through GUI also logs come
```
```bash
Edgecore file changes
vi /etc/kubeedge/config/edgecore.yaml

clusterDNS:
  - 169.254.96.16
  clusterDomain: "cluster.local"
      
metaServer:
  enable: true
```
```bash
Cloudcore file changes
LINK - https://github.com/kubeedge/kubeedge/blob/release-1.13/build/cloud/ha/02-ha-configmap.yaml.example
kubectl edit cm -n kubeedge cloudcore

dynamicController:   
  enable: true
```
