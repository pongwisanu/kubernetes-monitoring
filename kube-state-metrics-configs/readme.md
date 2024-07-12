# Create kube-state-metrics for Prometheus
1. Clone this project
2. Create all service and app for metrics
```
kubectl apply -f kube-state-metrics-configs
```
3. Check all pods healthy
```
kubectl get all -n kube-system
```
