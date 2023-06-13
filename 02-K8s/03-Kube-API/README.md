```
130  mkdir 03-Kube-API
  131  systemctl status kubelet
  132  ls
  133  kubectl  get pods -n kube-system
  134  cd /etc/kubernetes/
  135  ls
  136  cd manifests/
  137  s
  138  ls
  139  vim kube-apiserver.yaml
  140  ls
  141  apt-get install net-tools -y
  142  netstat -tulnp
  143  netstat -tulnp | grep -i kube
  144  kubectl  get pods -n kube-system
  145  kubectl cluster-info
  146  kubectl version
  147  kubectl version --short
  148  kubectl version --output=yaml
  149  kubectl api-versions
  150  kubectl api-resources
  151  ls
  152  cd
  153  ls
  154  kubectl  get nodes
  155  ip addr
  156  curl http://172.31.0.100:6443
  157  curl https://172.31.0.100:6443
  158  curl -k https://172.31.0.100:6443
  159  kubectl  get nodes
  160  cat .kube/config
  161  kubectl proxy --address='172.31.0.100' --port=8080 --accept-hosts='.' --accept-paths='.' &
  162  netstat -tulnp | grep -i 8080
  163  curl 172.31.0.100:8080
  164  curl 172.31.0.100:8080/api
  165  curl 172.31.0.100:8080/api/v1
  166  curl 172.31.0.100:8080/api/v1/pods
  167  curl 172.31.0.100:8080/api/v1/pods | grep -iA10 hello
  168  ls
  169  netstat -tulnp | grep -i 8080
  170  kill -9 9462
  171  netstat -tulnp | grep -i 8080
  172  ls
  173  kubectl config view
  174  kubectl config get-contexts
```
