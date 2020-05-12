## Steps

1. Applied deployment-k8stutorial-nginx-frontend.yaml

2. Applied service-k8stutorial-nodeport.yaml

3. Inspected the service:

```
$ kubectl describe service nodeportservice
Name:                     nodeportservice
Namespace:                default
Labels:                   <none>
Annotations:              Selector:  app=sa-frontend
Type:                     NodePort
IP:                       10.128.139.134
Port:                     http  80/TCP
TargetPort:               80/TCP
NodePort:                 http  32320/TCP
Endpoints:                10.2.0.6:80,10.2.0.7:80
Session Affinity:         None
External Traffic Policy:  Cluster
Events:                   <none>
```

NodePort:                 http  32320/TCP

is what told me I could hit this port 80 via port NodePort on my public ip addres at 32320

details came from: https://kubernetes.io/docs/concepts/configuration/overview/

# IT WORKED

## Roll one back just for fun:

```
kubectl rollout undo deployment sa-frontend
```
