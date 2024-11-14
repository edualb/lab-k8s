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
# ConfigMap
$ kubectl apply -f my-app.configmap.yaml
$ kubectl get configmap my-app-config -o yaml

# Pod
$ kubectl apply -f my-app.pod.yaml
$ kubectl logs my-app-pod -c myapp-container
$ kubectl logs my-app-pod -c sidecar-container
$ kubectl exec my-app-pod -c myapp-container -- cat /etc/config/config-file
```

# Clean up

```sh
$ kubectl delete pod my-app-pod
$ kubectl delete configmap my-app-config
```