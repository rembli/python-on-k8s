# Simple example to provision a python flask api for kubernetes deployment 

Source: https://betterprogramming.pub/getting-started-with-kubernetes-for-python-254d4c1d2041

### Deploy to K8S

Run in shell
> kubectl apply -f ./k8s

Use Port Forwarding to access apps in  cluster from browser
> kubectl port-forward -n python-on-k8s service/python-api 3000:3000 

Run in browser
> http://localhost:32020/

### Run K8s Dashboard

Run in shell
 > kubctl proxy
 
Start browser
> http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/#/overview?namespace=default

### Remove from cluster

Run in shell
> kubectl delete namespace python-on-k8s