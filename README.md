# jaitechltd-common-apps
Helm  releases for all applications, The package manager for Kubernetes

## Prerequisites
### Install Helm
```shell
brew install helm
```
### Install kubectl
```shell
brew install kubectl
```
### Install kubectx
```shell
brew install kubectx
```
### Install kubens
```shell
brew install kubens
```
### Install minikube
```shell
brew install minikube
```
### Minikube commands
```shell
minikube status
minikube start
minikube stop
minikube delete
minikube logs 
minikube dashboard
```
### Install k9s

https://k9scli.io/

```shell
brew install k9s
```

## Chart.yaml:

A Chart is a Helm package. It contains all of the resource definitions necessary to run an application, tool, or service inside of a Kubernetes cluster. Think of it like the Kubernetes equivalent of a Homebrew formula, an Apt dpkg, or a Yum RPM file.

## Release:

A Release is an instance of a chart running in a Kubernetes cluster. One chart can often be installed many times into the same cluster. And each time it is installed, a new release is created. Consider a MySQL chart. If you want two databases running in your cluster, you can install that chart twice. Each one will have its own release, which will in turn have its own release name.




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
```shell
helm template latlong-javaservice --namespace=jaitechltd > latlong-javaservice.yaml
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

```shell
helm install latlong-javaservice latlong-javaservice --namespace=jaitechltd
```

### Helm get list of releases

```shell
helm list --namespace=jaitechltd
```

Delete a release with the following command:

```shell
helm delete latlong --namespace=jaitechltd
```

```shell
helm delete latlong-javaservice --namespace=jaitechltd
```

# Kubernetes

Kubernetes get all contexts

```shell
kubectl config get-contexts
```

Switch to a context with the following command:

```shell
kubectl config use-context <context_name>
```
Example:
```shell
kubectl config use-context minikube
```
Create a new namespace with the following command:
```shell
kubectl create namespace <namespace>
```
Example:
```shell
kubectl create namespace jaitechltd

```
Get all namespaces with the following command:
```shell
 kubectl get namespace
```
Get all pods in a namespace with the following command:
```shell
kubectl get pods --namespace=jaitechltd
```

Get all pods in all namespaces with the following command:

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

## :e-mail: Contacts

Owner: [beemi.raja@gmail.com](beemi.raja@gmail.com)
