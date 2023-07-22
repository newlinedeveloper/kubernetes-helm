# kubernetes-helm
Developing and deploying helm charts on kubernetes

#### Prerequistics

```
- Docker setup: https://docs.docker.com/engine/install/
- Kubectl installation: https://kubernetes.io/docs/tasks/tools/
- Minikube setup : https://minikube.sigs.k8s.io/docs/start/
- helm setup  - https://helm.sh/docs/intro/install/

docker version

kubectl version

minikube version

helm version

minikube start
```


#### Helm Get started (Basics commands)

```
helm repo add bitnami https://charts.bitnami.com/bitnami

helm search repo bitnami

helm repo update 

helm install bitnami/mysql --generate-name

helm show chart bitnami/mysql

helm show all bitnami/mysql

helm list

helm uninstall mysql-1612624192

helm status mysql-1612624192

```



#### Artifacts Hub

```
https://artifacthub.io/packages/search

```


#### Multi Env deployment

```
# Dev env 
helm install helm-dev ./helm-chart --values ./helm-chart/env/dev/values.yml

helm uninstall helm-dev

# staging env
helm install helm-stage ./helm-chart --values ./helm-chart/env/stage/values.yml

helm uninstall helm-stage

# prod env
helm install helm-prod ./helm-chart --values ./helm-chart/env/prod/values.yml

helm uninstall helm-prod

```




#### Helm Commands

1. Deploying a web application using a Helm chart.

```
helm install myapp ./mychart
```

2. Updating a deployed application to a new version.

```
helm upgrade myapp ./mychart
```

3. Rolling back a deployment to a previous version..

```
helm rollback myapp 1
```

4.Installing a chart from a repository other than the default Helm Hub.

```
helm install myapp stable/mysql
```

5. Removing a deployed application and associated resources.

```
helm uninstall myapp
```

6. Providing custom configuration values for a chart during installation.

```
helm install myapp ./mychart --set app.port=8080 --set app.replicas=3
```
7. Getting a list of all the releases installed on a cluster.

```
helm list
```

8. Finding available charts related to a specific application or service.

```
helm search repo wordpress
```


9. Rendering the templates of a chart locally without installing it.

```
helm template ./mychart
```


10. Handling dependencies between multiple services or microservices.

```
helm dependency update ./mychart
```
