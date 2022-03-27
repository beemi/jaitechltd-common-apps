# jaitechltd-common-apps
Helm  releases for all applications

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
 kubectl get namespace
```

```shell
kubectl get pods --all
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


