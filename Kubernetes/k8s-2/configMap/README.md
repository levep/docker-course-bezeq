# [ConfigMaps](https://kubernetes.io/docs/concepts/configuration/configmap/)

```
kubectl create configmap my-config --from-file=simple-config.txt --from-literal=extra-param=extra-value --from-literal=another-param=another-value
```
```
kubectl create -f .\kuard-config.yaml

kubectl get configmaps my-config -o yaml

kubectl port-forward kuard-config 8080
```