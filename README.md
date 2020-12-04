# K8S Test Project

My K8S test project with Flask and Redis.

I decided to use the [Docker Compose sample project](https://docs.docker.com/compose/gettingstarted/) to get started with Kubernetes.

Components:
- Flask;
- Redis.

## Build the Docker image

Build the application Docker image with 
```
docker build -t <USERNAME>/k8sapp ./app
```
and push it to your Docker Registry.

Modify the `<USERNAME>` in the `k8s` directory in all configuration files containing it.

## Deploy

Deploy with Kubernetes:
```
kubectl apply -f k8s
```

## Secret

Create a secret in yout Kubernetes cluster with
```
kubectl create secret generic mypassword --from-literal PASSWORD=<YOURPASSWORDHERE>
```

Careful: this will be made public by the application (it's just a way to check the creation and working of secrets, actually, so I stupidly print them).
