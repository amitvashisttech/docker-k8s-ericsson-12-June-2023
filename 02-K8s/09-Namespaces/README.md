# NameSpace 

### List all the namespace 
```
kubectl get ns 
```

### Create a new namespace via command
```
kubectl create ns test
```

### Deploy the pods & check in which namespace its deployed. 
```
kubectl create -f 1-helloworld.yaml
```

```
kubectl get pods 
```


   21  kubectl get pods 
   22  
   23  kubectl create -f 2-Namespace-defination.yaml 
   24  kubectl create -f 1-helloworld.yaml -n myspace
   25  kubectl get deployment 
   26  kubectl get deployment -n myspace
   27  kubectl describe deployment helloworld-deployment -n myspace
   28  kubectl describe deployment helloworld-deployment 
   29  kubectl delete deployment helloworld-deployment -n myspace
   30  kubectl delete deployment helloworld-deployment 
   31  
   32  kubectl get deploy --all-namespaces
   33  
   34  kubectl create -f helloworld.yaml -n myspace -o yaml --dry=run
   35  kubectl create -f helloworld.yaml -n myspace -o yaml --dry-run
   36  kubectl create -f helloworld.yaml -n myspace -o yaml --dry-run >  helloworld-with-ns.yaml
 
   41  kubectl get deploy --all-namespaces

   43  kubectl delete -f 09-Namespaces/

