## Environment Setup 

### Step1 : Open the GitBash 

### Step2 : cd devops-lab/vagrant-setup/devops

### Step3 : Now check the Vagrant Status 
```
vagrant.exe status 
```

### Step4 : Bring up the virtalbox instances 
```
vagrant.exe up 
```

### Step5 : Let's Login to master node.
```
vagrant.exe ssh master 
```

### Step6 : Become a super user
```
sudo su - 
```

### Step7 : Clone the git project repo 
```
git clone https://github.com/amitvashisttech/docker-k8s-ericsson-12-June-2023.git
```

## Extra Vagrant Command  :
### Bring up a specific virtalbox instances 
```
vagrant.exe status 
vagrant.exe up master 
```
### Bring down a specific virtalbox instances 
```
vagrant.exe status 
vagrant.exe halt master 
```

### Destroy a specific virtalbox instances 
```
vagrant.exe status 
vagrant.exe destroy master 
```
