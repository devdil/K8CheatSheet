# K8CheatSheet
Kubernetes userful commands and cheat sheet

[Kubernetes Official Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

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
```
```
$ kubectl get pods
$ kubectl get pods --show-labels // get pods with labels
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

## Nodes
```
$ kubectl get pods -o wide
$ kubectl get pods -show-labels
$ kubectl describe node {nodename}

```
