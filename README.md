**CHANGES TO BE MADE**

01-ha-prepare.yaml- NO CHANGES
02-ha-configmap.yaml- (advertiseAddress - YOUR CLOUDCORE VIP HERE !!!, cloudStream: enable: false, dynamicController: enable: false)
03-ha-deployment.yaml- (nodeSelector: [key]: [value], image: kubeedge/cloudcore:{tag})
------------------------------------------------------------------------------------------------------
**#EXTRA ADDED IN 03-ha-deployment.yaml**

volumeMounts:
 - mountPath: /etc/kubeedge/certs/
   name: certificate
   readOnly: true
 - mountPath: /etc/kubeedge/ca/
   name: certificate1
   readOnly: true
   
volumes:
 - hostPath:
     path: /etc/kubeedge/certs/
     type: Directory
   name: certificate
 - hostPath:
     path: /etc/kubeedge/ca/
     type: Directory
   name: certificate1
---------------------------------------------------------------------------------------------------------
