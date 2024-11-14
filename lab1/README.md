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
$ kubectl apply -f my-nginx.pod.yaml
$ kubectl get pods
$ kubectl logs my-nginx-pod 
```

# Clean up

```sh
$ kubectl delete pod my-nginx-pod
```