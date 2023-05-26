# kubernetes-helm
Developing and deploying helm charts on kubernetes

#### Prerequistics

```
https://helm.sh/docs/intro/install/

helm version
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
