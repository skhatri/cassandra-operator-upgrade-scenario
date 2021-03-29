## Steps to Run Cassandra Operator

```
 kubectl create ns cassandra
 kubectl config set-context --current --namespace=cassandra

```

### Install operator and dc
```
##run this as admin
kubectl apply -f operator-role

helm install operator operator -f operator/values.yaml,operator/minikube.yaml

helm install dc dc -f dc/values.yaml,dc/minikube.yaml
```

### To Upgrade
Upgrade Operator
```
helm upgrade --install operator operator -f operator/values.yaml,operator/minikube.yaml

```
Let It restart Cassandra STS

Upgrade DC Custom Resource

```
helm upgrade --install dc dc -f dc/values.yaml,dc/minikube.yaml
```
