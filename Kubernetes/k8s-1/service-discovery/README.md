# [Service](https://kubernetes.io/docs/concepts/services-networking/service/)

## ClusterIP
```
kubectl create -f deployment-alpaca-prod.yaml
kubectl expose deployment alpaca-prod
```
```
kubectl get services -o wide
```

## NodePort
```
kubectl edit service alpaca-prod
```

#### Change the spec.type field to NodePort.
```
kubectl get services -o wide
```


## LoadBalancer
```
kubectl edit service alpaca-prod
```
#### Change the spec.type field to LoadBalancer.


