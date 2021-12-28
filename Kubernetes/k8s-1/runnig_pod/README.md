# [Pods](https://cloud.google.com/kubernetes-engine/docs/concepts/pod)
## Pod creation 

```
    kubectl create -f kuard-pod-full.yaml

    kubectl port-forward  --address 0.0.0.0 kuard  8080:8080
```

## kubectl exec

```
    kubectl exec kuard -- date

    kubectl exec -it kuard -- ash
```
## Pod health check

[Configure Liveness, Readiness and Startup Probes](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/)



## Resource Management
[Resource Management for Pods and Containers
](https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/)

 ## Persisting Data with Volimes
 [Persistent Volumes](https://kubernetes.io/docs/concepts/storage/persistent-volumes/)


## Labels and Selectors
[Labels and Selectors](https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/) 

```
$ cd lables
$ kubectl create -f .
```

```
kubectl get deployments --show-labels
kubectl label deployments alpaca-test "canary=true"
kubectl get deployments -L canary
kubectl label deployments alpaca-test "canary-"  # Remove label
kubectl get pods --show-labels
kubectl get pods --selector="ver=2"
kubectl get pods --selector="app=bandicoot,ver=2"
kubectl get pods --selector="app in (alpaca,bandicoot)"
kubectl get deployments --selector="canary"
```
### Cleanup 

```
kubectl delete deployments --all
```