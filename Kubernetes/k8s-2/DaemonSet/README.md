# [DaemonSet](https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/)

kubectl apply -f fluentd.yaml

kubectl describe daemonset fluentd

kubectl get pods -o wide

#### Limiting DaemonSets to Specific Nodes
The most common use case for DaemonSets is to run a Pod across every node in a
Kubernetes cluster. However, there are some cases where you want to deploy a Pod
to only a subset of nodes. For example, maybe you have a workload that requires a
GPU or access to fast storage only available on a subset of nodes in your cluster. In
cases like these node labels can be used to tag specific nodes that meet workload
requirements.

The first step in limiting DaemonSets to specific nodes is to add the desired set of
labels to a subset of nodes. This can be achieved using the kubectl label
command.
The following command adds the ssd=true label to a single node:
```
    kubectl label nodes k0-default-pool-35609c18-z7tb ssd=true

    kubectl apply -f nginx-fast-storage.yaml

    kubectl get pods -o wide
```
