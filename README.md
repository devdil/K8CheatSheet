# K8CheatSheet
Kubernetes userful commands and cheat sheet

## Kubernetes Cluster

Display kubernetes version both client and server
```
$ kubectl version
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
