## Steps to Run Cassandra Operator

```
##run this as admin
kubectl apply -f operator-role

helm install operator operator

helm install dc dc
```

### To Upgrade
Upgrade Operator
```
helm upgrade --install operator operator -f operator/values.yaml,operator/upgrade.yaml

```
Let It restart Cassandra STS

Upgrade DC Custom Resource

```
helm upgrade --install dc dc -f dc/values.yaml,dc/upgrade.yaml
```