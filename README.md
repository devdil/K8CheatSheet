# K8CheatSheet
Kubernetes userful commands and cheat sheet

# Containers

Copying files from and to containers
```
$ kubectl cp <podname>:/path/to/file/on/the/cotainer /local/file/path #from container
$ kubectl cp localfilepath <podname>:/path/on/the/container
```
