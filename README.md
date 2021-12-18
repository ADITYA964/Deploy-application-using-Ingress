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
Step 7:- Add the IP address of Ingress Dashboard followed by space and type "Adityas-website.com"

Step 8:- Application deployed as Kubernetes service using Ingress by going to http://Adityas-Website.com

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Deploy application using Ingress from Docker image

Step 1:-
```shell
minikube start --vm-driver=docker
```
Step 2:-
```shell
minikube addons enable ingress
```
Step 3:-
```shell
kubectl get pods -n ingress-nginx
```
Step 4:-
```shell
kubectl create deployment prostate-app --image=adityax123/adityas-docker-images:1.0.0
```
Step 5:-
```shell
kubectl expose deployment prostate-app--type=LoadBalancer --port=80 --target-port 8501
```

Step 6:-
```shell
kubectl get service prostate-cancer-service-two 
```
Step 7:-
```shell
minikube service prostate-cancer-service-two --url 
```
