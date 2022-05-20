# memcached-operator
Based on Quickstart for Go-based Operators https://sdk.operatorframework.io/docs/building-operators/golang/quickstart/

## Initialize the project
```shell
operator-sdk init --domain salteddog --repo github.com/flopotok/memcached-operator
```

## Create Memcached API
```shell
operator-sdk create api --group cache --version v1alpha1 --kind Memcached --resource --controller
```

## Build and push operator image
```shell
make docker-build docker-push IMG="salteddog/memcached-operator:v0.0.1"
```