```
  678  cd 02-K8s/
  679  ls
  680  cd 12-Service-Discovery/
  681  ls
  682  cat secrets.yaml
  683  cat database.yaml
  684  ls
  685  cat database-service.yml
  686  ls
  687  kubectl apply -f secrets.yaml
  688  kubectl apply -f database.yaml
  689  kubectl apply -f database-service.yml
  690  ls
  691  cat helloworld-app-deployment.yml
  692  kubectl  get svc
  693  ls
  694  kubectl get pods
  695  kubectl delete -f ../10-Wordpress-Multi-Container-Pod/
  696  ls
  697  kubectl apply -f helloworld-app-deployment.yml
  698  kubectl apply -f helloworld-app-svc.yml
  699  cat helloworld-app-svc.yml
  700  kubectl get pods
  701  cat helloworld-app-deployment.yml
  702  cat helloworld-app-svc.yml
  703  kubectl get pods
  704  kubectl  get svc
  705  curl 172.31.0.101:32621
  706  kubectl  get pods
  707  kubectl exec -it database -- mysql -u root -p
  708  kubectl  get pods
  709  kubectl exec -it helloworld-deployment-7c557cd984-74jpl -- env

```


## MySQL DB Commands 
```
kubectl exec -it database -- mysql -u root -p
```
```
Enter password:
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 2
Server version: 5.7.42 MySQL Community Server (GPL)

Copyright (c) 2000, 2023, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
mysql>
```

### Check the Databases
```
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| helloworld         |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0.04 sec)
```

### Switch the Database to helloworld:
```
mysql> use helloworld;
Database changed
```

### Check the table space in helloworld DB:
```
mysql> show tables;
Empty set (0.00 sec)
```


### After hello application is deployed, check the table & visit count:
```
mysql> show tables;
+----------------------+
| Tables_in_helloworld |
+----------------------+
| visits               |
+----------------------+
1 row in set (0.01 sec)
```

```
mysql> select * from visits;
+----+---------------+exit 
| id | ts            |
+----+---------------+
|  1 | 1686909084758 |
+----+---------------+
1 row in set (0.27 sec)
```

```
exit
```
