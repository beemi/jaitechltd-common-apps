# jaitechltd-common-apps
Helm  releases for all applications, The package manager for Kubernetes

## Chart.yaml:

A Chart is a Helm package. It contains all of the resource definitions necessary to run an application, tool, or service inside of a Kubernetes cluster. Think of it like the Kubernetes equivalent of a Homebrew formula, an Apt dpkg, or a Yum RPM file.

## Release:

A Release is an instance of a chart running in a Kubernetes cluster. One chart can often be installed many times into the same cluster. And each time it is installed, a new release is created. Consider a MySQL chart. If you want two databases running in your cluster, you can install that chart twice. Each one will have its own release, which will in turn have its own release name.


### Install helm
```shell
curl https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3 | bash   
```
```shell
brew install helm
```

create a new helm chart with the following command:

```shell
helm create latlong-app --namespace=jaitechltd
```

Chart.yaml

values.yaml

deployment.yaml

service.yaml


### Helm template

```shell
helm template latlong-app --namespace=jaitechltd > latlong-app.yaml
```

### Helm lint
```shell
helm lint latlong-app.yaml
```

### Helm dry run
```shell
helm install latlong-app --debug --dry-run latlong-app
```

### Helm install

install a chart with the following command:

```shell
helm install latlong latlong-app --namespace=jaitechltd
```

### Helm get list of releases

```shell
helm list --namespace=jaitechltd
```

Delete a release with the following command:

```shell
helm delete latlong-app --namespace=jaitechltd
```

# Kubernetes

```shell
kubectl create namespace <namespace>
```

```shell
kubectl create namespace jaitechltd

```

```shell
 kubectl get namespace
```

```shell
kubectl get pods --namespace=jaitechltd
```

kubernetes get deployments
```shell
kubectl get deployments
```

Delete pods from a namespace

```shell
kuectl delete pods --all --namespace=jaitechltd
```

```shell
kubectl delete pod <pod_name> --namespace=jaitechltd
```


