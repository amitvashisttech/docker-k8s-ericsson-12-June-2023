# Deploy Calico 

## Configure Docker Image Pull Secrets
```
docker login 

kubectl create secret generic regcred --from-file=.dockerconfigjson=/root/.docker/config.json --type=kubernetes.io/dockerconfigjson -n kube-system
```

## Deploy Calico
```
kubectl apply -f calico.yaml
```

## Now wait for all the calico pods to come up. 
```
kubectl get pods -n kube-system -o wide 
```

## Let's delete old proxy, coredns & other pods.

## Now check all the pod IP Address should be fall in 192.168.0.0/16 range. 
