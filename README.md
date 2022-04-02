# coldstart-performance-testing

Testing container startup times on Kubernetes

We use a custom version of [podspeed](https://github.com/markusthoemmes/podspeed) to do our benchmarking. 

## Steps

* Clone [Kubernetes](https://github.com/kubernetes/kubernetes)
* Make you code changes
* Spin up a cluster using [hack/local-up-cluster.sh](https://github.com/kubernetes/kubernetes/blob/master/hack/local-up-cluster.sh)
* Run `podspeed` to benchmark how long it takes a pod to get ready, for example:

``` bash
podspeed -prepull -pods 10 -template probe-milliseconds.yaml
```

