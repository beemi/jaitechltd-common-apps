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
