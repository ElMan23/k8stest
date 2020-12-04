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
