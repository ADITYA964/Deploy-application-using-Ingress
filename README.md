# Deploy-application-using-Ingress

Requirements

Step 1:- Install Ingress Controller in Minikube

```shell
minikube addons enable ingress
```
Step 2:- Check Ingress Pod

```shell
kubectl get pod -n kube-system
```
