# Apache2-Docker
Httpd Deployment with Configmap

### Clone this repo

### Copy httpd.conf file of your configuration to this location


### Create configmap from your httpd.conf
```
kubectl create configmap httpd-conf --from-file=httpd.conf --dry-run=client -o yaml > httpd-conf.yaml
```


### After creating configmap from the above command run the following commands to deploy to your cluster

```
kubectl apply -f httpd-conf.yaml
kubectl apply -f service.yaml
kubectl apply -f deployment.yaml
```



