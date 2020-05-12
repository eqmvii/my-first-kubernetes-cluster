# Testing a cluster on linode

WOOOOOOOO

## base config

To configure access:

```
export KUBECONFIG=~/repos/test-k8s-cluster-linode/testcluster-kubeconfig.yaml
```

Persistent: https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/#set-the-kubeconfig-environment-variable

## Configuration

```
kubectl config get-contexts
```

# TODO

The rest of the tutorial pods, perhaps?

https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/
