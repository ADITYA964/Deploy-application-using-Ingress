# Deploy-application-using-Ingress

Step 1:- Install Ingress Controller in Minikube

```shell
minikube addons enable ingress
```
Step 2:- Check Ingress Pod

```shell
kubectl get pod -n kube-system
```
Step 3:- Create Ingress Rule

```shell
kubectl apply -f dashboard-ingress.yaml
```

Step 4:- Check Ingress Dashboard

```shell
kubectl get ingress -n kubernetes-dashboard
```
Step 5:- Copy the Ingress Dashboard address

Step 6:- Procedure to edit hosts file in Windows
```shell
choco install nano   # If nano is not installed

cd C:\Windows\System32\drivers\etc

ls

nano hosts
```
