# kubernetes in 2 hours (V 2.0)

- [1. Understanding Kubernetes](#understanding-kubernetes)
- [2. Creating your own Kubernetes environment](#creating-your-own-kubernetes-environment)
- [3. Understanding kubernetes management and API resources](#understanding-kubernetes-management-and-API-resources)
- [4. Pods and Deployments](#pods-and-deployments)
- [5. Troubleshooting applications](#troubleshooting-applications)
- [6. Understanding service and demo](#understanding-service-and-demo)
- [7. Understanding Volumes and demo](#understanding-volumes-and-demo)
- [8. Understading config maps and demo](#understanding-config-maps-and-demo)

## 1.
##  Understanding Kubernetes








## 2.
## Creating your own Kubernetes environment
### Minikube environment DEMO


## 3.
## Understanding kubernetes management and API resources

### kubectl
 ```
 kubectl create deploy mynginx --image=nginx --replicas=3
 ```
### Use kubectl get to get information about running applications
```
kubectl get all
kubectl get pods
kubectl get all --selector app=mynginx
```

### Use kubectl describe to get information about resource properties
```
kubectl describe pod mynginx-aaa-bbb
```

Get current state of an object: kubectl get deployments nginx -o yaml
* Push settings from a new manifest: 
```
kubectl create -f nginx.yaml
```
* Apply settings from a manifest: 
```
kubectl apply -f nginx.yaml
```
* Generating yaml files :
```
kubectl create deploy mynginx --image=nginx --dry-run=client -o yaml > mypod.yaml t
```

## 4.
## Pods and Deployments


## 5.
##  Troubleshooting applications
* kubectl describe pods
* kubectl logs
* kubectl get pods
* kubectl exec

### DEMO
```
kubectl create deploy mydb --image=mariadb --replicas=3
```
```
kubectl describe pod mydb-aaa-bbb
```
```
kubectl logs mydb-aaa-bbb
```
```
kubectl set env deploy/mydb MARIADB_ROOT_PASSWORD=secret
```

## 6.
## Understanding service and demo

### SERVICE DEMO

* creating deployment
```
kubectl create deployment nginxsvc --image=nginx
```
* Scaling Deployment
```
kubectl scale deployment nginxsvc --replicas=3
```
* Exposing Service
```
kubectl expose deployment nginxsvc --port=80
```
* Service IP details
```
kubectl describe svc nginxsvc 
```
* Service details
```
kubectl get svc
```

* List endpoints
```
kubectl get endpoints
```

![](https://github.com/chirag99969/kubernetes/blob/main/image/Untitled.jpg)


## 7.
##  Understanding Volumes and demo
![](https://github.com/chirag99969/kubernetes/blob/main/image/Untitled%20(1).jpg)


## 8.
##  Understading config maps and demo



