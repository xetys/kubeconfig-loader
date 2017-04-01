## Simple kubeconfig switcher

**Why do I did this project?**

I know there is the *cool* way of dealing with multiple k8s clusters, by merging the different kube-configs in `~/.kube/config` and use `kubectl config use-context` to switch them. Currently I'm setting up a lot of clusters, with their own kubeconfigs, and I'm getting tired of all that merging.

Actually, life can be simpler just by rotating that configs around. So I spent that 10 minutes of bashing that project to make my (and maybe your) life easier.

## How to install?

* clone that project
* put it into a folder behind your $PATH, like `/usr/bin`, `/usr/local/bin` or what ever you want
* you are done...it's simple bash, and does not depend on any lib

## How to use?

whenever a wild kubeconfig appears, add it with

```
$ kubeconfig-loader add my-new-cluster /path/to/new/kubeconfig/file
```

proof you have `my-new-cluster` available with

```
$ kubeconfig-loader ls
```

switch to that cluster by

```
$ kubeconfig-loader use my-new-cluster
```

and check it works with

```
$ kubectl get node
```

or any other kubectl related command


***happy kubing***


