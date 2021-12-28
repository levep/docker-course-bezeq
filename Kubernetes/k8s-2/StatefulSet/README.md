# [StatefulSet](https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/)
```
kubectl apply -f web.yaml
kubectl get service nginx
kubectl get statefulset
kubectl get pod
```
```
kubectl get pvc

kubectl scale sts web --replicas=5
```
---
``` 
kubectl delete sts web
kubectl delete sts web --cascade=false
```