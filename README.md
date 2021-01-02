# K8CheatSheet
Kubernetes userful commands and cheat sheet

# Kubernetes Cluster

Display kubernetes version both client and server
```
$ kubectl version
```

# Containers

Copying files from and to containers
```
$ kubectl cp <podname>:/path/to/file/on/the/cotainer /local/file/path #from container
$ kubectl cp localfilepath <podname>:/path/on/the/container
```
Viewing logs from containers
```
$ kubectl logs <podname>
$ kubectl logs <podname> -f # similar variant of tail -f 
```

Pods

get pods

```
$ kubectl get pods
```

get pods with labels

```
$ kubectl get pods --show-labels
```
