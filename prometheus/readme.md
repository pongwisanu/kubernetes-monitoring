# Prometheus Install on kubernetes cluster

1. Create namespace
```
kubectl create namespace monitoring
```
2. Create RBAC role from file **clusterRole.yaml**
```
kubectl create -f clusterRole.yaml
```
3. Create Prometheus configuration from file **confg-map.yaml**
```
kubectl create -f config-map.yaml
```
4. Create Prometheus deployment from file **deployment.yaml**
```
kubectl create -f deployment.yaml

kubectl get all -n monitoring ###check is pod healthy
```
5. Make prometheus accessible from file **service.yaml** (nodeport)
```
kubectl create -f service.yaml
```
then access at port 30000
