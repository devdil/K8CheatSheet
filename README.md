# K8CheatSheet
Kubernetes userful commands and cheat sheet

[Kubernetes Official Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

[Kubernetes Unofficial Cheat Sheet](https://unofficial-kubernetes.readthedocs.io/en/latest/user-guide/kubectl-cheatsheet/)

[Kubernetes Internals Tutorial](https://www.youtube.com/watch?v=3KtEAa7_duA)

## Kubernetes Cluster

Display kubernetes version both client and server
```
$ kubectl version #displays kubernetes both client and server
$ kubectl cluster-info # dispalys cluster stats
```

## Pods

```
$ kubectl cp <podname>:/path/to/file/on/the/cotainer /local/file/path // copy files from container
$ kubectl cp localfilepath <podname>:/path/on/the/container // copy files to container
```
```
$ kubectl logs <podname> // view logs
$ kubectl logs <podname> -f // similar variant of tail -f
$ kubectl logs [pod-name] -c [container-name] // if more than one container
$ kubectl logs [pod-name] --all-containers=true
$ kubectl logs -p [pod-name] // previous pod
```
```
$ kubectl get pods
$ kubectl get pods --show-labels // get pods with labels
$ kubectl describe pod podname -n namepsace 
```
```
$ kubectl get pods --selector="<labelName>=<labelValue>" // filter by labename whose value is labelvalue
$ kubectl get pods --selector="<labelName>=<labelValue>,<label2Name>=<label2Value>" // multiple labels together
$ kubectl get pods --selector="!<labelName>" // key not set
$ kubectl get pods --selector=<labelName> in (value1, value2)" // either satisfies value1, value2
$ kubectl get pods --selector=<labelName> notin (value1, value2)" // not in all of these values
$ kubectl get pods --selector=<labelname>!=<value> // labelname not equals value
$ kubectl get pods --l 'labelname>=<value>' // shortcut for labelname

```
```
$ kubectl describe pod [pod-name] //get event details of the pod
$ kubectl exec [pod-name] -it sh
```
## Nodes
```
$ kubectl get nodes -o wide
$ kubectl get nodes -show-labels
$ kubectl describe node {nodename}

```

# Everything
```
$ kubectl get all -o wide
```

# Utilization
```
$ kubectl top pods -n namespace
$ kubectl top nodes -n namespace
$ kubectl top pods --all-namespaces
$ kubectl top pod <pod_name> --containers


```
