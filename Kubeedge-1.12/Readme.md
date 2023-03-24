```bash
1). In cat /etc/kubeedge/config/edgecore.yaml
clusterDNS:
  - 169.254.96.16
  clusterDomain: "cluster.local"
Responsible for net not working on the edge server (Microservice net not working mozilla firefox)

2. In edgemesh-agent-cfg (hub server configmap kubeedge ns)
edgeProxy:
  enable: true 
because of this microservice is able to open through GUI (Microservice)

3. In cat /etc/kubeedge/config/edgecore.yaml
edgeStream:
  enable: true
Responsible for events on the edge server (Microservice events)
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
