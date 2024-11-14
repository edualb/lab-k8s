# Dependencies

- [minikube](https://minikube.sigs.k8s.io/docs/start/?arch=%2Flinux%2Fx86-64%2Fstable%2Fbinary+download#Ingress)
- [docker](https://docs.docker.com/engine/install/ubuntu/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)

# Setup

```sh
$ minikube start
```

# Lab

```sh

$ kubectl apply -f myapp.deployment.yaml
$ kubectl rollout status deployment myapp-deployment
$ kubectl describe deploy myapp-deployment

$ kubectl rollout restart deployment myapp-deployment
$ kubectl rollout status deployment myapp-deployment

$ kubectl scale deployment myapp-deployment --replicas=5
$ kubectl get deployments


$ kubectl get rs
$ kubectl scale rs <replica-set-name> --replicas=2
$ kubectl get rs
```

# Clean up

```sh
$ kubectl delete deployment myapp-deployment
```