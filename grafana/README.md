# Create Grafana for Prometheus Virtualization
1. Create config map
```
kubectl create -f grafana-datasource-config.yaml
```
2. Create PV for grafana in this case use nfs 
```
vi pv.yaml
## change nfs path and nfs server

kubectl create -f pv.yaml
```
3. Create deployment
```
kubectl create -f deployment.yaml
```
4. Make Grafana access from outside (nodeport)
```
kubectl create -f service.yaml
```
access at port 32000
