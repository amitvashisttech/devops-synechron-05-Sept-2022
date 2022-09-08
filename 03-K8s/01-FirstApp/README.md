# Creating out First App

## Check the health of Cluster
```
kubectl get nodes
```

## Deploy Nginx App
```
kubectl run hello-k8s --image=nginx --port=80
```

## Check the status of PODs
```
kubectl get pods
kubectl describe pods hello-k8s
```

Note Point : In Case you are getting imagepull error stating that you have reached to max limit of downloads, then apply the following solution. 

# Docker login
```
docker login
ls /root/.docker/config.json
```

# Create a Secret in K8s for Docker Registry
```
kubectl create secret generic regcred --from-file=.dockerconfigjson=/root/.docker/config.json --type=kubernetes.io/dockerconfigjson

kubectl get secrets
```


## Now Genrate Nginx Deployment Config:
```
kubectl run hello-k8s --image=nginx --port=80 --dry-run -o yaml > nginx.yaml
```

## Update the Pull Defination in Yaml File 
```
      imagePullSecrets:
      - name: regcred
```

## Now we can deploy nginx with Pull Secrets
```
kubectl apply -f nginx.yaml
```


```
kubectl get pods
NAME             READY   STATUS    RESTARTS   AGE
hello-k8s        1/1     Running   0          6m22s
```
